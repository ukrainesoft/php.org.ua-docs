---
navigation:
  - install.pecl.windows.md: « Встановлення PHP-модуля у Windows
  - install.pecl.phpize.md: 'Компіляція модулів, що розділяються, за допомогою phpize »'
  - index.md: PHP Manual
  - install.pecl.md: Встановлення модулів PECL
title: 'Компіляція модулів, що розділяються за допомогою команди pecl'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Компіляція модулів, що розділяються за допомогою команди pecl

PECL полегшує створення загальнодоступних модулів PHP. Виконайте наступну [»Команда pecl](https://pear.php.net/manual/en/guide.users.commandline.cli.php) :

$ pecl install extname

Ця команда завантажить вихідний код для модуля *extname*, скомпілює та встановить файл extname.so у директорію [extension\_dir](ini.core.md#ini.extension-dir). Потім файл extname.so може бути завантажений через php.ini

По умолчанию команда`pecl` не встановлюватиме пакети, зазначені станом `alpha`или`beta`. Якщо немає доступних стабільних (`stable`) версій пакетів, можна встановити `beta`\-версію пакета наступною командою:

$ pecl install extname-beta

Також можна встановити певну версію, вказавши команду так:

$ pecl install extname-0.1

> **Зауваження** :
> 
> Після підключення модуля у файлі php.ini необхідно перезапустити веб-сервер, щоб зміни набули чинності.
