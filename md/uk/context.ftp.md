---
navigation:
  - context.http.md: « Опції контексту HTTP
  - context.ssl.md: Опції контексту SSL »
  - index.md: PHP Manual
  - context.md: Контекстні опції та параметри
title: Параметри контексту FTP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Параметри контексту FTP

Параметри контексту FTP — Список параметрів контексту FTP

### Опис

Параметри контексту для транспортних протоколів `ftp://`и`ftps://`

### Опції

`overwrite`bool

Дозволяє перезаписувати наявні файли на віддаленому сервері. Працює лише у режимі запису (upload).

По умолчанию\*\*`false`\*\*

`resume_pos`int

Зміщення у файлі, з якого розпочинається передача. Працює лише у режимі читання (download).

По умолчанию (Начало файла).

`proxy`string

FTP-запит через проксі-сервер HTTP. Застосовується лише під час операції читання файлу. Приклад: `tcp://squid.example.com:8000`

### Примітки

> **Зауваження** **Опції контексту нижчого потоку в сокеті**  
> Додаткові опції контексту можуть підтримуватись [нижчим транспортним протоколом](transports.inet.md). Для потоків `ftp://`, це стосується опцій контексту для транспортного протоколу `tcp://`. Для потоків `ftps://`, це стосується опцій контексту для транспортного протоколу `ssl://`

### Дивіться також

-   [ftp://](wrappers.ftp.md)
-   [Контекстні опції сокету](context.socket.md)
-   [Опції контексту SSL](context.ssl.md)
