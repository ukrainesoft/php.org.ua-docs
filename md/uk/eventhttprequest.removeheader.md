---
navigation:
  - eventhttprequest.geturi.md: '« EventHttpRequest::getUri'
  - eventhttprequest.senderror.md: 'EventHttpRequest::sendError »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::removeHeader'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::removeHeader

(PECL event >= 1.4.0-beta)

EventHttpRequest::removeHeader — Видаляє заголовок HTTP із заголовків запиту

### Опис

```methodsynopsis
public
   EventHttpRequest::removeHeader(
    string
     $key
   , 
    string
     $type
   ): void
```

Видаляє заголовок HTTP із заголовків запиту.

### Список параметрів

`key`

Назва заголовка.

`type`

`type`одна из констант`EventHttpRequest::*_HEADER`

### Значення, що повертаються

Видаляє заголовок HTTP із заголовків запиту.

### Дивіться також

-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) \- Додає заголовок HTTP до заголовків запиту
