Конструктор об'єкта EventHttpRequest

-   [« EventHttpRequest::closeConnection](eventhttprequest.closeconnection.md)
    
-   [EventHttpRequest::findHeader »](eventhttprequest.findheader.md)
    
-   [PHP Manual](index.md)
    
-   [EventHttpRequest](class.eventhttprequest.md)
    
-   Конструктор об'єкта EventHttpRequest
    

# EventHttpRequest::construct

(PECL event >= 1.4.0-beta)

EventHttpRequest::construct — Конструктор об'єкта EventHttpRequest

### Опис

```methodsynopsis
public
   EventHttpRequest::__construct(
    callable
     $callback
   , 
    mixed
     $data
     = null
   )
```

Конструктор об'єкта EventHttpRequest.

### Список параметрів

`callback`

Викликається за запитом шляху. Повинен відповідати наступному прототипу:

```methodsynopsis
callback(
       EventHttpRequest
        $req
        = null
      , 
       mixed
        $arg
        = null
      ): void
```

`data`

Користувальницькі дані, що передаються в callback-функцію.

### Значення, що повертаються

Повертає об'єкт EventHttpRequest.

### Приклади

**Приклад #1 Приклад **EventHttpRequest::construct()****

```php
<?php

function _request_handler($req, $base) {
    echo __FUNCTION__, PHP_EOL;

    if (is_null($req)) {
        echo "Время вышло\n";
    } else {
        $response_code = $req->getResponseCode();

        if ($response_code == 0) {
            echo "Соединение разорвано\n";
        } elseif ($response_code != 200) {
            echo "Неожиданный ответ: $response_code\n";
        } else {
            echo "Успешно: $response_code\n";
            $buf = $req->getInputBuffer();
            echo "Тело ответа:\n";
            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
                echo $s, PHP_EOL;
            }
        }
    }

    $base->exit(NULL);
}


$address = "127.0.0.1";
$port = 80;

$base = new EventBase();
$conn = new EventHttpConnection($base, NULL, $address, $port);
$conn->setTimeout(5);
$req = new EventHttpRequest("_request_handler", $base);

$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);
$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);
$conn->makeRequest($req, EventHttpRequest::CMD_GET, "/index.cphp");

$base->loop();
?>
```

### Дивіться також

-   [EventHttpRequest::cancel()](eventhttprequest.cancel.md) - Скасує очікування HTTP-запиту
-   [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) - Додає заголовок HTTP до заголовків запиту