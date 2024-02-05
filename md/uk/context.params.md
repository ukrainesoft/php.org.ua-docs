---
navigation:
  - context.phar.md: « Контекстні опції Phar
  - context.zip.md: Опції контексту Zip »
  - index.md: PHP Manual
  - context.md: Контекстні опції та параметри
title: Параметри контексту
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Параметри контексту

Параметри контексту — Список параметрів контексту

### Опис

Ці параметри можуть бути задані для контексту за допомогою функції [stream\_context\_set\_params()](function.stream-context-set-params.md)

### Список параметрів

`notification` [callable](language.types.callable.md)

Функция типа[callable](language.types.callable.md), що викликається при настанні події у потоці.

За подробностями обращайтесь к документации функции[stream\_notification\_callback](function.stream-notification-callback.md)
