---
navigation:
  - eventhttprequest.removeheader.md: '« EventHttpRequest::removeHeader'
  - eventhttprequest.sendreply.md: 'EventHttpRequest::sendReply »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::sendError'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Краткое описание ошибки. Если\*\*`null`\*\*, використовуватиметься стандартне значення коду помилки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**EventHttpRequest::sendError()\*\*\*\*

```php
<?php
function _http_400($req) {
    $req->sendError(400);
}

$base = new EventBase();
$http = new EventHttp($base);

$http->setCallback("/err400", "_http_400");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

### Дивіться також

-   [EventHttpRequest::sendReply()](eventhttprequest.sendreply.md) \- Відправляє HTML-відповідь клієнту
