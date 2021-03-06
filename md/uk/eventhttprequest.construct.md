- [« EventHttpRequest::closeConnection](eventhttprequest.closeconnection.md)
- [EventHttpRequest::findHeader »](eventhttprequest.findheader.md)

- [PHP Manual](index.md)
- [EventHttpRequest](class.eventhttprequest.md)
- Конструктор об'єкту EventHttpRequest

# EventHttpRequest::\_\_construct

(PECL event \>= 1.4.0-beta)

EventHttpRequest::\_\_construct — Конструктор об'єкта EventHttpRequest

### Опис

public **EventHttpRequest::\_\_construct**(
[callable](language.types.callable.md) `$callback` ,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$data` = **`null`** )

Конструктор об'єкта EventHttpRequest.

### Список параметрів

`callback`
Викликається за запитом шляху. Повинен відповідати наступному
прототипу:

**callback**( [EventHttpRequest](class.eventhttprequest.md) `$req` =
**`null`** ,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$arg` = **`null`** ): void

`data`
Користувальницькі дані, що передаються в callback-функцію.

### Значення, що повертаються

Повертає об'єкт EventHttpRequest.

### Приклади

**Приклад #1 Приклад **EventHttpRequest::\_\_construct()****

` <?phpfunction _request_handler($req, $base) {   echo __FUNCTION__, PHP_EOL; if (is_null($req)) {        echo "Час вийшло
";  |                                             
";         } elseif ($response_code != 200) {             echo "Несподівана відповідь: $response_code
";        } else {            echo "Успішно: $response_code
";             $buf = $req->getInputBuffer();            echo "Тіло відповіді:
";            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {                echo $s, PHP_EOL;            }        }    }    $base->exit(NULL);}$address = "127.0.0.1";$port = 80;$base = new EventBase();$conn = new EventHttpConnection($base, NULL, $address, $port);$conn->setTimeout(5);$req = new EventHttpRequest("_ );$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);$conn->ma req, EventHttpRequest::CMD_GET, "/index.cphp");$base->loop();?> `

### Дивіться також

- [EventHttpRequest::cancel()](eventhttprequest.cancel.md) -
Скасує очікування HTTP-запиту
- [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) -
Додає заголовок HTTP до заголовків запиту
