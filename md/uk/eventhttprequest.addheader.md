---
navigation:
  - class.eventhttprequest.md: « EventHttpRequest
  - eventhttprequest.cancel.md: 'EventHttpRequest::cancel »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
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

Одна з констант [`EventHttpRequest::*_HEADER`](class.eventhttprequest.md#eventhttprequest.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventHttpRequest::removeHeader()](eventhttprequest.removeheader.md) - Видаляє заголовок HTTP із заголовків запиту
