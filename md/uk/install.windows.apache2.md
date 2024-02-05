---
navigation:
  - install.windows.commandline.md: Командний рядок PHP у Microsoft Windows
  - install.windows.troubleshooting.md: Стандартні проблеми PHP під Windows »
  - index.md: PHP Manual
  - install.windows.md: Встановлення у системах Windows
title: Apache 2.x у Microsoft Windows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Apache 2.x у Microsoft Windows

Цей розділ містить примітки та підказки до інсталяції PHP, пов'язаної з Apache 2.x на системах Microsoft Windows.

> **Зауваження** :
> 
> Спочатку слід прочитати [кроки ручної установки](install.windows.manual.md)!

Крайне рекомендуется обратиться к[» Документації Apache](http://httpd.apache.org/docs/current/), щоб отримати базове уявлення про сервер Apache 2.x. Також подумайте про читання [»  Примітки для Windows](http://httpd.apache.org/docs/current/platform/windows.md) для Apache 2.x перед читанням цього посібника.

Загрузите последнюю версию[» Apache 2.x](https://www.apachelounge.com/download/)и подходящую версию PHP. Следуйте[крокам ручної установки](install.windows.manual.md) і повертайтеся, щоб продовжити інтеграцію PHP та Apache.

Існує три способи налаштувати PHP для роботи з Apache 2.x у Windows. PHP можна запускати як обробник, як CGI або під FastCGI.

> **Зауваження**: Пам'ятайте, що при вказівці шляхів у конфігураційних файлах Apache під Windows всі зворотні сліші, наприклад, c:\\directory\\file.ext повинні змінюватися на прямі: c:/directory/file.ext. Для шляхів з директоріями також може знадобитися сліш наприкінці.

### Встановлення як оброблювач Apache

Щоб завантажити PHP-модуль для Apache 2.x, необхідно вставити наступні рядки у файл конфігурації Apache httpd.conf:

**Приклад #1 PHP і Apache 2.x як оброблювач**

\# до PHP 8.0.0 ім'я модуля було php7\_module LoadModule php\_module "c:/php/php8apache2\_4.dll" <FilesMatch \\.php$> SetHandler application/x-httpd-php

# вкажіть шлях до php.ini

PHPIniDir "C:/php"

> **Зауваження**: У наведених вище прикладах необхідно підставити фактичний шлях до PHP замість C:/php/. Переконайтеся, що файл, вказаний у директиві `LoadModule`, знаходився у вказаному місці. Використовуйте php7apache2\_4.dll для PHP 7 або php8apache2\_4.dll для PHP 8.

### Запуск PHP як CGI

Настійно рекомендується звернутися до [» Документації Apache CGI](http://httpd.apache.org/docs/current/howto/cgi.md) для більш повного розуміння того, як запускати CGI в Apache.

Щоб запустити PHP як CGI, файли php-cgi повинні бути поміщені до каталогу, позначеного як каталог CGI з використанням директиви ScriptAlias.

Строку`#!` необхідно буде помістити файли PHP, які вказують на розташування бінарного файлу PHP:

**Приклад #2 PHP та Apache 2.x як CGI**

```
#!C:/php/php.exe
<?php
  phpinfo();
?>
```

**Увага**

Використовуючи інсталяцію CGI, сервер відкритий перед кількома можливими вразливістю. Будь ласка, ознайомтесь із розділом «[Безпека CGI](security.cgi-bin.md)» щоб дізнатися, як можна захистити себе від таких атак.

### Запуск PHP під FastCGI

Запуск PHP під FastCGI має низку переваг перед запуском як CGI. Налаштування в такий спосіб досить просте:

Загрузите`mod_fcgid`с[» https://www.apachelounge.com](https://www.apachelounge.com/download/). Бінарні файли Win32 доступні для завантаження цього сайту. Встановіть модуль відповідно до інструкції, що додається.

Налаштуйте свій веб-сервер, як показано нижче, подбавши про те, щоб скоригувати всі шляхи відповідно до того, як ви провели інсталяцію у своїй конкретній системі:

**Приклад #3 Налаштування Apache для запуску PHP як FastCGI**

```
LoadModule fcgid_module modules/mod_fcgid.so
# Где находится ваш файл php.ini?
FcgidInitialEnv PHPRC        "c:/php"
<FilesMatch \.php$>
    SetHandler fcgid-script
</FilesMatch>
FcgidWrapper "c:/php/php-cgi.exe" .php
```

Файли з розширенням .php тепер виконуватимуться обгорткою PHP FastCGI.
