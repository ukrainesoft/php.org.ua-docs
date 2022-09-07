---
navigation:
  - install.unix.lighttpd-14.md: « Установка PHP на Lighttpd 1.4 на Unix-системах
  - install.unix.commandline.md: Установка з інтерфейсами CGI та командного рядка »
  - index.md: PHP Manual
  - install.unix.md: Встановлення на Unix-системи
title: Веб-сервер LiteSpeed/OpenLiteSpeed ​​на системах Unix
---
## Веб-сервер LiteSpeed/OpenLiteSpeed ​​на системах Unix

LiteSpeed ​​PHP – це оптимізована збірка PHP для роботи з продуктами LiteSpeed ​​через LiteSpeed ​​SAPI. LSPHP запускається як самостійний процес і має окремий файл, що виконується, який використовується як звичайний виконуваний файл командного рядка для запуску скриптів PHP.

LSAPI – це дуже оптимізований API, що дозволяє LiteSpeed ​​взаємодіяти з веб-движками інших виробників. Він має той самий протокол, що і FCGI, але набагато ефективніший.

Ця документація містить інструкції з встановлення та конфігурування PHP з LSAPI для веб-серверів LiteSpeed ​​(LSWS) і OpenLiteSpeed ​​(OLS).

Цей посібник передбачає, що LSWS або OLS встановлені за стандартними шляхами та зі стандартними прапорами. Директорія установки за замовчуванням для обох веб-серверів - /usr/local/lsws, і вони запускаються з її підкаталогу bin.

Зверніть увагу, що у всій документації номери версій замінені на `x`, Що говорить про те, що ця документація залишиться актуальною і в майбутньому. Тому сміливо можете замінити ці символи на номер вашої версії.

1.  Для отримання та встановлення LSWS та OLS відвідайте сайт із документацією по LiteSpeed ​​Web Server - [» инструкции по установке](https://docs.litespeedtech.com/products/lsws/installation/) або сайт з документацією по OpenLiteSpeed ​​- [» инструкции по установке](https://openlitespeed.org/kb/category/installation/more-installation-methods/)
    
2.  Завантажте та розпакуйте вихідні коди PHP:
    
    ```
    mkdir /home/php
    cd /home/php
    wget http://us1.php.net/get/php-x.x.x.tar.gz/from/this/mirror
    tar -zxvf php-x.x.x.tar.gz
    cd php-x.x.x
    ```
    
3.  Налаштуйте та зберіть PHP. На цьому етапі можна скористатися додатковими опціями для більш тонкого налаштування PHP та додавання необхідних модулів. Запустіть ./configure --help, щоб отримати список можливих опцій. У наведеному нижче прикладі використовуються стандартні рекомендовані налаштування для LSWS:
    
    ```
    ./configure ... '--with-litespeed'
    make
    sudo make install
    ```
    
4.  Перевірте встановлення LSPHP
    
    Один із найпростіших шляхів для перевірки коректності установки PHP – це запустити наступні команди:
    
    ```
    cd /usr/local/lsws/fcgi-bin/
    ./lsphp5 -v
    ```
    
    Повинна з'явитися інформація про збірку PHP:
    
    ```
    PHP 5.6.17 (litespeed) (built: Mar 22 2016 11:34:19)
    Copyright (c) 1997-2014 The PHP Group
    Zend Engine v2.6.0, Copyright (c) 1998-2015 Zend Technologies
    ```
    
    Зверніть увагу на слово `litespeed`. Це означає, що PHP зібраний за допомогою LSAPI.
    

Після виконання описаних вище кроків, LSWS/OLS повинні запускатися за допомогою PHP як модуля SAPI. Існує досить багато додаткових опцій конфігурації для налаштування роботи LSWS/OLS c PHP. Більш детально почитати про них можна на сайті з документацією LiteSpeed ​​в розділі [» PHP](https://docs.litespeedtech.com/extapp/php/configuration/control/)

Використання LSPHP з командного рядка:

Режим командного рядка LSPHP(LSAPI + PHP) використовується для обробки скриптів PHP, запущених на віддаленому сервері без необхідності тримати на ньому веб-сервер. Це використовується для обробки скриптів PHP на локальному веб-сервері (роздільно). Така установка зручна для зручності масштабування, оскільки навантаження обробки скриптів лягає на віддалений сервер.

Запустіть lsphp з командного рядка на віддаленому сервері: LSPHP - є файлом, що виконується, може бути запущений вручну і прив'язаний до IPv4, IPv6 або сокету Unix за допомогою опції -b socketaddress.

Приклад:

Прив'язка LSPHP до порту 3000 на всіх інтерфейсах IPv4 та IPv6:

```
/path/to/lsphp -b [::]:3000
```

Прив'язка LSPHP до 3000 всіх інтерфейсів IPv4:

```
/path/to/lsphp -b *:3000
```

Прив'язка LSPHP до 192.168.0.2:3000:

```
/path/to/lsphp -b 192.168.0.2:3000
```

Прив'язка LSPHP до сокету Unix `/tmp/lsphp_manual.sock` з можливістю отримувати з нього запити:

```
/path/to/lsphp -b /tmp/lsphp_manual.sock
```

Перед запуском LSPHP можна виставити змінні оточення:

```
PHP_LSAPI_MAX_REQUESTS=500 PHP_LSAPI_CHILDREN=35 /path/to/lsphp -b IP_address:port
```

На даний момент LiteSpeed ​​PHP можна використовувати з веб-серверами LiteSpeed, OpenLiteSpeed ​​та Apache modlsapi. Подробиці про конфігурацію сервера читайте на сторінках [» LiteSpeed Web Server](https://docs.litespeedtech.com/extapp/php/getting_started/) і [» OpenLiteSpeed](https://openlitespeed.org/kb/category/installation/php-installation-guides/)

LSPHP можна встановити різними способами.

CentOS: На CentOS, LSPHP може бути встановлений з репозиторіїв LiteSpeed ​​або Remi, використовуючи [» RPM](https://docs.litespeedtech.com/extapp/php/getting_started/#litespeed-repo-search-packages)

Debian: На Debian, LSPHP можна поставити з репозиторію LiteSpeed, використовуючи [» apt](https://docs.litespeedtech.com/extapp/php/getting_started/#litespeed-repo-search-packages)

cPanel: Для встановлення з cPanel та LSWS/OLS використовуючи EasyApache 4, читайте відповідну [» документацию](https://docs.litespeedtech.com/cp/cpanel/quickstart/#easyapache-integration)

Plesk: Plesk можна використовувати з LSPHP на CentOS, CloudLinux, Debian та Ubuntu. Докладніше описано в [» документации](https://docs.litespeedtech.com/cp/plesk/)
