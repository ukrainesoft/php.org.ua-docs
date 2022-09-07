---
navigation:
  - install.windows.commandline.md: Командний рядок PHP у Microsoft Windows
  - install.windows.troubleshooting.md: Стандартні проблеми PHP під Windows »
  - index.md: PHP Manual
  - install.windows.md: Установка в системах Windows
title: Apache 2.x у Microsoft Windows
---
## Apache 2.x у Microsoft Windows

Цей розділ містить примітки та підказки до інсталяції PHP, пов'язаної з Apache 2.x на системах Microsoft Windows.

> **Зауваження**
> 
> Спочатку слід прочитати [шаги ручной установки](install.windows.manual.md)

Вкрай рекомендується звернутися до [»  Документации Apache](http://httpd.apache.org/docs/current/), щоб отримати базове уявлення про сервер Apache 2.x. Також подумайте про читання [»  Примечаний для Windows](http://httpd.apache.org/docs/current/platform/windows.md) для Apache 2.x перед читанням цього посібника.

Завантажте останню версію [» Apache 2.x](https://www.apachelounge.com/download/) та відповідну версію PHP. Дотримуйтесь [шагам ручной установки](install.windows.manual.md) і повертайтеся, щоб продовжити інтеграцію PHP та Apache.

Існує три способи налаштувати PHP для роботи з Apache 2.x у Windows. PHP можна запускати як обробник, як CGI або під FastCGI.

> **Зауваження**: Пам'ятайте, що при вказівці шляхів у конфігураційних файлах Apache під Windows всі зворотні сліші, наприклад, c:directoryfile.ext повинні змінюватися на прямі: c:/directory/file.ext. Для шляхів з директоріями також може знадобитися сліш наприкінці.

### Встановлення як оброблювач Apache

Щоб завантажити модуль PHP для Apache 2.x, необхідно вставити наступні рядки у файл конфігурації Apache httpd.conf:

**Приклад #1 PHP і Apache 2.x як оброблювач**

до PHP 8.0.0 ім'я модуля було php7module LoadModule phpmodule "c:/php/php8apache24.dll" SetHandler application/x-httpd-php

# вкажіть шлях до php.ini

PHPIniDir "C:/php"

> **Зауваження**: У наведених вище прикладах необхідно підставити фактичний шлях до PHP замість C:/php/. Переконайтеся, що файл, вказаний у директиві `LoadModule`, знаходився у вказаному місці. Використовуйте php7apache24.dll для PHP 7 або php8apache24.dll для PHP 8.

### Запуск PHP як CGI

Настійно рекомендується звернутися до [» Документации Apache CGI](http://httpd.apache.org/docs/current/howto/cgi.md) для більш повного розуміння того, як запускати CGI в Apache.

Щоб запустити PHP як CGI, файли php-cgi повинні бути поміщені до каталогу, позначеного як каталог CGI з використанням директиви ScriptAlias.

Рядок `#!` необхідно буде помістити файли PHP, які вказують на розташування бінарного файлу PHP:

**Приклад #2 PHP та Apache 2.x як CGI**

```
#!C:/php/php.exe
<?php
  phpinfo();
?>
```

**Увага**

Використовуючи інсталяцію CGI, ваш сервер відкритий перед кількома можливими вразливістю. Будь ласка, ознайомтесь із розділом ["Безпека CGI"](security.cgi-bin.md) щоб дізнатися, як можна захистити себе від таких атак.

### Запуск PHP під FastCGI

Запуск PHP під FastCGI має низку переваг перед запуском як CGI. Налаштування в такий спосіб досить просте:

Завантажте `mod_fcgid` з [» https://www.apachelounge.com](https://www.apachelounge.com/download/). Бінарні файли Win32 доступні для завантаження цього сайту. Встановіть модуль відповідно до інструкції, що додається.

Налаштуйте свій веб-сервер, як показано нижче, подбавши про те, щоб усі шляхи відображали те, як ви провели установку у своїй конкретній системі:

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
