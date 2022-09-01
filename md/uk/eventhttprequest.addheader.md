---
navigation:
  - class.eventhttprequest.html: « EventHttpRequest
  - eventhttprequest.cancel.html: 'EventHttpRequest::cancel »'
  - index.html: PHP Manual
  - class.eventhttprequest.html: EventHttpRequest
title: 'EventHttpRequest::addHeader'
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

Одна з констант [`EventHttpRequest::*_HEADER`](class.eventhttprequest.html#eventhttprequest.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventHttpRequest::removeHeader()](eventhttprequest.removeheader.md) - Видаляє заголовок HTTP із заголовків запиту
