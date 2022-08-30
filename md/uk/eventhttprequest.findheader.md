Отримує значення заголовка

-   [« EventHttpRequest::construct](eventhttprequest.construct.md)
    
-   [EventHttpRequest::free »](eventhttprequest.free.md)
    
-   [PHP Manual](index.md)
    
-   [EventHttpRequest](class.eventhttprequest.md)
    
-   Отримує значення заголовка
    

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

Одна з констант [`EventHttpRequest::*_HEADER`](class.eventhttprequest.html#eventhttprequest.constants)

### Значення, що повертаються

Повертає \*\*`null`\*\*якщо заголовок не знайдено.

### Дивіться також

-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) - Додає заголовок HTTP до заголовків запиту