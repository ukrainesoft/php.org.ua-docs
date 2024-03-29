---
navigation:
  - context.zlib.md: « Zlib context options
  - wrappers.file.md: 'file:// »'
  - index.md: PHP Manual
  - langref.md: Довідник мови
title: Підтримувані протоколи та обгортки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Підтримувані протоколи та обгортки

PHP поставляється з багатьма вбудованими обгортками для різних URL-протоколів для використання з функціями файлової системи, таких як [fopen()](function.fopen.md) [copy()](function.copy.md) [file\_exists()](function.file-exists.md) і [filesize()](function.filesize.md). Крім цих обгорток, можна реєструвати власні обгортки, використовуючи функцію [stream\_wrapper\_register()](function.stream-wrapper-register.md)

> **Зауваження**: URL синтаксис, що використовується для опису обгортки, може бути тільки виду `scheme://...`. Варіанти синтаксису `scheme:/`и`scheme:` не підтримуються.

## Зміст

-   [file://](wrappers.file.md)— Доступ до локальної файлової системи
-   [http://](wrappers.http.md)— Доступ до URL-адрес за протоколом HTTP(s)
-   [ftp://](wrappers.ftp.md)— Доступ до URL-адрес за протоколом FTP(s)
-   [php://](wrappers.php.md)— Доступ до різних потоків введення-виводу
-   [zlib://](wrappers.compression.md)— Стислі потоки
-   [data://](wrappers.data.md) \- Схема Data (RFC 2397)
-   [glob://](wrappers.glob.md)— Знаходження шляхів, що відповідають шаблону
-   [phar://](wrappers.phar.md) \- PHP-архів
-   [ssh2://](wrappers.ssh2.md)— Secure Shell 2
-   [rar://](wrappers.rar.md)— RAR
-   [ogg://](wrappers.audio.md) \- Аудіопотоки
-   [expect://](wrappers.expect.md)— Потоки для взаємодії з процесами
