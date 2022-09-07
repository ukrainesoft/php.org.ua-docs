---
navigation:
  - install.unix.apache2.md: Apache 2.x на Unix системах
  - install.unix.lighttpd-14.md: Установка PHP на Lighttpd 1.4 на Unix-системах »
  - index.md: PHP Manual
  - install.unix.md: Встановлення на Unix-системи
title: Встановлення Nginx 1.4.x на систему Unix
---
## Встановлення Nginx 1.4.x на систему Unix

Ця документація описує процес встановлення та налаштування PHP з PHP-FPM для Nginx 1.4.x HTTP сервера.

Даний посібник передбачає, що ви зібрали Nginx з вихідних кодів, отже, всі бінарні файли та файли конфігурації розташовуються в `/usr/local/nginx`. Якщо ні, і ви отримали Nginx іншим способом, тоді, будь ласка, зверніться до [» Nginx Wiki](https://www.nginx.com/resources/wiki/), щоб перекласти цей посібник для вашої установки.

Цей посібник охоплює ази налаштування Nginx сервера, для обробки PHP додатків та відображення їх на порту 80. Рекомендується вивчити документацію Nginx і PHP-FPM, якщо ви хочете оптимізувати вашу установку за рамками даної документації.

Будь ласка, зверніть увагу, що в цій документації номери версій були замінені на 'x', щоб ця документація залишалася коректною в майбутньому. Будь ласка, замініть 'x' на необхідний номер версії.

1.  Рекомендується відвідати [» страницу установки](https://www.nginx.com/resources/wiki/start/topics/tutorials/install/) на Nginx Wiki, для інформації про отримання та встановлення Nginx.
    
2.  Отримання та розпакування вихідні коди PHP:
    
    ```
    tar zxf php-x.x.x
    ```
    
3.  Налаштування та збирання PHP. У цьому розділі описано налаштування та збирання PHP з вихідних кодів. Запустіть ./configure --help, щоб отримати список доступних опцій. У нашому прикладі ми зробимо прості налаштування з PHP-FPM та підтримкою MySQLi.
    
    ```
    cd ../php-x.x.x
    ./configure --enable-fpm --with-mysqli
    make
    sudo make install
    ```
    
4.  Переміщення файлів налаштування в потрібні директорії
    
    ```
    cp php.ini-development /usr/local/php/php.ini
    cp /usr/local/etc/php-fpm.d/www.conf.default /usr/local/etc/php-fpm.d/www.conf
    cp sapi/fpm/php-fpm /usr/local/bin
    ```
    
5.  Важливо, що ми забороняємо Nginx від надсилати запити до бекенду PHP-FPM, якщо файл не існує, що допомагає уникнути атаки ін'єкції скрипта.
    
    Ми можемо виправити це шляхом встановлення директиви [cgi.fixpathinfo](ini.core.md#ini.cgi.fix-pathinfo) рівною `0` у нашому php.ini файлі.
    
    Редагування php.ini:
    
    ```
    vim /usr/local/php/php.ini
    ```
    
    Знайдіть опцію `cgi.fix_pathinfo=` і змініть її так:
    
    ```
    cgi.fix_pathinfo=0
    ```
    
6.  php-fpm.conf повинен бути модифікований, щоб точно визначити, що php-fpm повинен працювати під користувачем www-data та групою www-data до того, як ми запустимо сервіс:
    
    ```
    vim /usr/local/etc/php-fpm.d/www.conf
    ```
    
    Знайдіть та зміните наступне:
    
    ```
    ; Unix user/group of processes
    ; Замечание: Пользователь является обязательным. Если группа не установлена,
    ; то будет использована стандартная группа пользователя.
    user = www-data
    group = www-data
    ```
    
    Тепер можна запускати сервіс php-fpm:
    
    ```
    /usr/local/bin/php-fpm
    ```
    
    Більше в цьому посібнику ми не будемо стосуватися налаштування php-fpm. Якщо вам необхідно зробити додаткові налаштування - зверніться до документації php-fpm.
    
7.  Тепер Nginx має бути налаштований на підтримку виконання PHP:
    
    ```
    vim /usr/local/nginx/conf/nginx.conf
    ```
    
    Змініть блок "location", заданий за умовчанням, так, щоб можна було обробляти файли .php:
    
    location / { root html; index index.php index.html index.htm; }
    
    Наступний крок – переконатися, що .php файли відправляються в бекенд PHP-FPM. Введіть наступне:
    
    location ~ .php$ { fastcgiindex index.php; fastcgipass 127.0.0.1: 9000; include fastcgiparams; fastcgiparam SCRIPTFILENAME $documentroot$fastcgiscriptname; fastcgiparam SCRIPTNAME $fastcgiscriptname; }
    
    Перезапустіть Nginx.
    
    ```
    sudo /usr/local/nginx/sbin/nginx -s stop
    sudo /usr/local/nginx/sbin/nginx
    ```
    
8.  Створіть тестовий файл
    
    ```
    rm /usr/local/nginx/html/index.html
    echo "<?php phpinfo(); ?>" >> /usr/local/nginx/html/index.php
    ```
    
    Тепер відкрийте у браузері [http://localhost](http://localhost). Відобразиться інформація phpinfo().
    

Дотримуючись вищезгаданих кроків, ви отримаєте робочий Nginx сервер з підтримкою PHP як модуля `FPM` `SAPI`. Звичайно, доступна велика кількість опцій налаштувань для Nginx та PHP. Для більш детальної інформації наберіть **./configure --help** у відповідному дереві вихідних кодів.
