---
navigation:
  - install.pecl.windows.html: « Установка PHP-модуля в Windows
  - install.pecl.phpize.html: 'Компіляція модулів, що розділяються, за допомогою phpize »'
  - index.html: PHP Manual
  - install.pecl.html: Установка модулей PECL
title: 'Компіляція модулів, що розділяються за допомогою команди pecl'
---
## Компіляція модулів, що розділяються за допомогою команди pecl

PECL дозволяє легко створювати модулі PHP, що розділяються. Використовуючи [» команду pecl](https://pear.php.net/manual/en/guide.users.commandline.cli.php), виконайте таке:

$pecl install extname

Ця команда завантажить вихідний код для модуля *extname*, скомпілює та встановить extname.so у вашу директорію [extensiondir](ini.core.html#ini.extension-dir). Файл extname.so може бути завантажений у php.ini

За замовчуванням команда `pecl` не встановлюватиме пакети, зазначені станом `alpha` або `beta`. Якщо немає доступних стабільних (`stable`) версій пакетів, ви можете встановити `beta`версію пакета, використовуючи наступну команду:

$pecl install extname-beta

Також, ви можете встановити певну версію, використовуючи такий варіант:

$pecl install extname-0.1

> **Зауваження**
> 
> Після підключення модуля в php.ini необхідно перезапустити веб-сервер для того, щоб зміни набули чинності.
