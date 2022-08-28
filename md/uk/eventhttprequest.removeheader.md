Видаляє заголовок HTTP із заголовків запиту

-   [« EventHttpRequest::getUri](eventhttprequest.geturi.html)
    
-   [EventHttpRequest::sendError »](eventhttprequest.senderror.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttpRequest](class.eventhttprequest.html)
    
-   Видаляє заголовок HTTP із заголовків запиту
    

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

`type` одна з констант `EventHttpRequest::*_HEADER`

### Значення, що повертаються

Видаляє заголовок HTTP із заголовків запиту.

### Дивіться також

-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.html) - Додає заголовок HTTP до заголовків запиту