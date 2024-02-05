---
navigation:
  - configuration.file.md: « Файл конфігурації
  - configuration.changes.modes.md: Місця встановлення параметрів конфігурації »
  - index.md: PHP Manual
  - configuration.md: Конфігурація часу виконання
title: Файли .user.ini
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Файли .user.ini

Включено підтримку INI-файлів у стилі .htaccess на рівні каталогу. Ці файли обробляються *тільки* CGI/FastCGI SAPI. Ця функція робить непотрібним модуль PECL htscanner. Якщо PHP працює як модуль Apache, то для досягнення того ж ефекту працюють з файлами .htaccess.

На додаток до основного файлу php.ini PHP шукає INI-файли в кожній директорії, починаючи з директорії запитаного PHP-файлу і продовжує пошук до кореневої директорії (встановленої в елементі [$\_SERVER\['DOCUMENT\_ROOT'\]](reserved.variables.server.md)). Якщо PHP-файл лежить поза кореневою директорією, то сканується лише його директорія.

Тільки INI-налаштування з режимами **`INI_PERDIR`** і **`INI_USER`** будуть розпізнані в INI-файлах у стилі .user.ini.

Дві нові INI-директиви, [user\_ini.filename](ini.core.md#ini.user-ini.filename) і [user\_ini.cache\_ttl](ini.core.md#ini.user-ini.cache-ttl), контролюють використання INI-файлів користувача.

[user\_ini.filename](ini.core.md#ini.user-ini.filename) встановлює ім'я файлу, за яким PHP здійснює пошук у кожній директорії; якщо встановлений порожній рядок, то PHP пошук не здійснює. За замовчуванням `.user.ini`

[user\_ini.cache\_ttl](ini.core.md#ini.user-ini.cache-ttl) встановлює наскільки часто INI-файли користувача будуть оновлюватися. За промовчанням період оновлення становить 300 секунд (5 хвилин).
