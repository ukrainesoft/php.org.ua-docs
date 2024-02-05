---
navigation:
  - class.eventhttprequest.md: « EventHttpRequest
  - eventhttprequest.cancel.md: 'EventHttpRequest::cancel »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::addHeader'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::addHeader

(PECL event >= 1.4.0-beta)

EventHttpRequest::addHeader — Додає заголовок HTTP до заголовків запиту

### Опис

```methodsynopsis
public
   EventHttpRequest::addHeader(
    string
     $key
   , 
    string
     $value
   , 
    int
     $type
   ): bool
```

Додає заголовок HTTP до заголовків запиту.

### Список параметрів

`key`

Назва заголовка.

`value`

Значення заголовка.

`type`

Одна из констант[`EventHttpRequest::*_HEADER`](class.eventhttprequest.md#eventhttprequest.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventHttpRequest::removeHeader()](eventhttprequest.removeheader.md) \- Видаляє заголовок HTTP із заголовків запиту
