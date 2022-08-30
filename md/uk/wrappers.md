Підтримувані протоколи та обгортки

-   [« Опции контекста Zip](context.zip.html)
    
-   [file:// »](wrappers.file.html)
    
-   [PHP Manual](index.html)
    
-   [Справочник языка](langref.html)
    
-   Підтримувані протоколи та обгортки
    

# Підтримувані протоколи та обгортки

PHP поставляється з багатьма вбудованими обгортками для різних URL-протоколів для використання з функціями файлової системи, таких як [fopen()](function.fopen.html) [copy()](function.copy.html) [fileexists()](function.file-exists.html) і [filesize()](function.filesize.html). Крім цих обгорток, можна реєструвати власні обгортки, використовуючи функцію [streamwrapperregister()](function.stream-wrapper-register.html)

> **Зауваження**: URL синтаксис, що використовується для опису обгортки, може бути тільки виду `scheme://...`. Варіанти синтаксису `scheme:/` і `scheme:` не підтримуються.

## Зміст

-   [file://](wrappers.file.html) — Доступ до локальної файлової системи
-   [http://](wrappers.http.html) — Доступ до URL-адрес за протоколом HTTP(s)
-   [ftp://](wrappers.ftp.html) — Доступ до URL-адрес за протоколом FTP(s)
-   [php://](wrappers.php.html) — Доступ до різних потоків введення-виводу
-   [zlib://](wrappers.compression.html) — Стислі потоки
-   [data://](wrappers.data.html) - Схема Data (RFC 2397)
-   [glob://](wrappers.glob.html) — Знаходження шляхів, що відповідають шаблону
-   [phar://](wrappers.phar.html) - PHP-архів
-   [ssh2://](wrappers.ssh2.html) - Secure Shell 2
-   [rar://](wrappers.rar.html) - RAR
-   [ogg://](wrappers.audio.html) - Аудіопотоки
-   [expect://](wrappers.expect.html) — Потоки для взаємодії з процесами