Файли .user.ini

-   [« Файл конфигурации](configuration.file.md)
    
-   [Де можуть бути встановлені параметри конфігурації »](configuration.changes.modes.md)
    
-   [PHP Manual](index.md)
    
-   [Конфігурація часу виконання](configuration.md)
    
-   Файли .user.ini
    

## Файли .user.ini

Включено підтримку INI-файлів у стилі .htaccess на рівні каталогу. Ці файли обробляються *тільки* CGI/FastCGI SAPI. Ця функція робить непотрібним модуль PECL htscanner. Якщо ви використовуєте PHP як модуль Apache, то для досягнення того ж ефекту використовуйте файли .htaccess.

Крім основного файлу php.ini, PHP шукає INI-файли в кожній директорії, починаючи з директорії запитаного PHP-файлу і продовжує пошук до кореневої директорії (встановленої в [SERVER\['DOCUMENTROOT'\]](reserved.variables.server.md)). Якщо PHP-файл знаходиться поза кореневою директорією, то сканується лише його директорія.

Тільки INI-налаштування з режимами **`PHP_INI_PERDIR`** і **`PHP_INI_USER`** будуть розпізнані в INI-файлах у стилі .user.ini.

Дві нові INI-директиви, [userini.filename](ini.core.html#ini.user-ini.filename) і [userini.cachettl](ini.core.html#ini.user-ini.cache-ttl), контролюють використання INI-файлів користувача.

[userini.filename](ini.core.html#ini.user-ini.filename) встановлює ім'я файлу, за яким PHP здійснює пошук у кожній директорії; якщо встановлений порожній рядок, то PHP пошук не здійснює. За замовчуванням `.user.ini`

[userini.cachettl](ini.core.html#ini.user-ini.cache-ttl) встановлює наскільки часто користувачі INI-файли будуть оновлюватися. За промовчанням період оновлення становить 300 секунд (5 хвилин).