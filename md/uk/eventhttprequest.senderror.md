Надсилає HTML-повідомлення про помилку клієнту

-   [« EventHttpRequest::removeHeader](eventhttprequest.removeheader.html)
    
-   [EventHttpRequest::sendReply »](eventhttprequest.sendreply.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttpRequest](class.eventhttprequest.html)
    
-   Надсилає HTML-повідомлення про помилку клієнту
    

# EventHttpRequest::sendError

(PECL event >= 1.4.0-beta)

EventHttpRequest::sendError — Надсилає HTML-повідомлення про помилку клієнту

### Опис

```methodsynopsis
public
   EventHttpRequest::sendError(
    int
     $error
   , 
    string
     $reason
     = null
   ): void
```

Надсилає HTML-повідомлення про помилку клієнту.

### Список параметрів

`error`

HTTP код помилки.

`reason`

Короткий опис помилки. Якщо **`null`**, використовуватиметься стандартне значення коду помилки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **EventHttpRequest::sendError()****

```php
<?php
function _http_400($req) {
    $req->sendError(400);
}

$base = new EventBase();
$http = new EventHttp($base);

$http->setCallback("/err400", "_http_400");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

### Дивіться також

-   [EventHttpRequest::sendReply()](eventhttprequest.sendreply.html) - Відправляє HTML-відповідь клієнту