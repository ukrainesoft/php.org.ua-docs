---
navigation:
  - eventhttprequest.construct.md: '« EventHttpRequest::\_\_construct'
  - eventhttprequest.free.md: 'EventHttpRequest::free »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::findHeader'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::findHeader

(PECL event >= 1.4.0-beta)

EventHttpRequest::findHeader — Отримує значення заголовка

### Опис

```methodsynopsis
public
   EventHttpRequest::findHeader(
    string
     $key
   , 
    string
     $type
   ): void
```

Отримує значення заголовка

### Список параметрів

`key`

Назва заголовка.

`type`

Одна из констант[`EventHttpRequest::*_HEADER`](class.eventhttprequest.md#eventhttprequest.constants)

### Значення, що повертаються

Повертає \*\*`null`\*\*якщо заголовок не знайдено.

### Дивіться також

-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) \- Додає заголовок HTTP до заголовків запиту
