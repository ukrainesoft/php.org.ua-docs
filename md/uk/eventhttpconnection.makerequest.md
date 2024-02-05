---
navigation:
  - eventhttpconnection.getpeer.md: '« EventHttpConnection::getPeer'
  - eventhttpconnection.setclosecallback.md: 'EventHttpConnection::setCloseCallback »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::makeRequest'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpConnection::makeRequest

(PECL event >= 1.4.0-beta)

EventHttpConnection::makeRequest — Робить HTTP-запит із зазначеного з'єднання.

### Опис

```methodsynopsis
public
   EventHttpConnection::makeRequest(
    EventHttpRequest
     $req
   , 
    int
     $type
   , 
    string
     $uri
   ): bool
```

Робить HTTP-запит із зазначеного з'єднання . `type`одна из констант`EventHttpRequest::CMD_*`

### Список параметрів

`req`

Об'єкт підключення, через який надсилається запит.

`type`

одна из констант[`EventHttpRequest::CMD_*`](class.eventhttprequest.md#eventhttprequest.constants)

`uri`

URI, пов'язаний із запитом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** EventHttpConnection::makeRequest()\*\*\*\*

```php
<?php
function _request_handler($req, $base) {
    echo __FUNCTION__, PHP_EOL;

    if (is_null($req)) {
        echo "Время вышло\n";
    } else {
        $response_code = $req->getResponseCode();

        if ($response_code == 0) {
            echo "Соединение разорвано\n";
        } elseif ($response_code != 200) {
            echo "Неожиданный ответ: $response_code\n";
        } else {
            echo "Успешно: $response_code\n";
            $buf = $req->getInputBuffer();
            echo "Тело ответа:\n";
            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
                echo $s, PHP_EOL;
            }
        }
    }

    $base->exit(NULL);
}

$address = "127.0.0.1";
$port = 80;

$base = new EventBase();
$conn = new EventHttpConnection($base, NULL, $address, $port);
$conn->setTimeout(5);
$req = new EventHttpRequest("_request_handler", $base);

$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);
$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);
$conn->makeRequest($req, EventHttpRequest::CMD_GET, "/index.cphp");

$base->loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
_request_handler
Success: 200
Body:
PHP, date:
2013-03-13T20:27:52+05:00
```

### Дивіться також

-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) \- Додає заголовок HTTP до заголовків запиту
