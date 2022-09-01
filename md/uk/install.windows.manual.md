---
navigation:
  - install.windows.recommended.md: « Рекомендована конфігурація для Windows
  - install.windows.building.md: Складання з вихідних кодів »
  - index.md: PHP Manual
  - install.windows.md: Установка в системах Windows
title: Самостійне встановлення PHP у Windows
---
## Самостійне встановлення PHP у Windows

### Виберіть веб-сервер

#### IIS

IIS є вбудованим у Windows. Використовуйте Server Manager для додавання ролі IIS на сервері Windows. Переконайтеся, що функцію CGI увімкнено. На робочому столі Windows використовуйте панель "Встановлення та видалення програм" для додавання IIS. У документації Microsoft є [» детальні інструкції](https://docs.microsoft.com/en-us/previous-versions/ms181052(v=vs.80)). Для настільних веб-застосунків та веб-розробки можна також використовувати IIS/Express або робочий стіл PHP.

**Приклад #1 Командний рядок для налаштування IIS та PHP**

```
@echo off

REM download .ZIP file of PHP build from http://windows.php.net/downloads/

REM path to directory you decompressed PHP .ZIP file into (no trailing \)
set phppath=c:\php


REM Clear current PHP handlers
%windir%\system32\inetsrv\appcmd clear config /section:system.webServer/fastCGI
REM The following command will generate an error message if PHP is not installed. This can be ignored.
%windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /-[name='PHP_via_FastCGI']

REM Set up the PHP handler
%windir%\system32\inetsrv\appcmd set config /section:system.webServer/fastCGI /+[fullPath='%phppath%\php-cgi.exe']
%windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /+[name='PHP_via_FastCGI',path='*.php',verb='*',modules='FastCgiModule',scriptProcessor='%phppath%\php-cgi.exe',resourceType='Unspecified']
%windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /accessPolicy:Read,Script

REM Configure FastCGI Variables
%windir%\system32\inetsrv\appcmd set config -section:system.webServer/fastCgi /[fullPath='%phppath%\php-cgi.exe'].instanceMaxRequests:10000
%windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phppath%\php-cgi.exe'].environmentVariables.[name='PHP_FCGI_MAX_REQUESTS',value='10000']"
%windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phppath%\php-cgi.exe'].environmentVariables.[name='PHPRC',value='%phppath%\php.ini']"
```

#### Apache

Існує кілька версій Apache2 для Windows. Ми підтримуємо ApacheLounge, але інші варіанти включають XAMPP, WampServer та BitNami, які надають засоби автоматичної установки. Ви можете використовувати modphp або modfastcgi для завантаження PHP на Apache Якщо ви використовуєте modphp необхідно використовувати TS-build Apache, Visual C тієї ж версії і той же процесор (x86 або x64).

### Виберіть збірку

Завантажте PHP-релізи з [» http://windows.php.net/download/](http://windows.php.net/download/). Усі зборки оптимізовані (PGO), а випуски QA та GA ретельно протестовані.

Є 4 типи збірок PHP:

-   Thread-Safe(TS) - для одного процесу веб-служб, як Apache з modphp
    
-   Non-Thread-Safe(NTS) - для служб IIS та інших FastCGI веб-серверів (Apache з modfastcgi) рекомендується і для сценаріїв командного рядка
    
-   для x86 – для 32-розрядної версії
    
-   для x64 – для 64-розрядної версії
