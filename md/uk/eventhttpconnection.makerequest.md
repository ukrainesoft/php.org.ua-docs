- [«EventHttpConnection::getPeer](eventhttpconnection.getpeer.md)
- [EventHttpConnection::setCloseCallback »](eventhttpconnection.setclosecallback.md)

- [PHP Manual](index.md)
- [EventHttpConnection](class.eventhttpconnection.md)
- Робить HTTP-запит із зазначеного з'єднання

# EventHttpConnection::makeRequest

(PECL event \>= 1.4.0-beta)

EventHttpConnection::makeRequest — Робить HTTP-запит по вказаному
з'єднанню

### Опис

public **EventHttpConnection::makeRequest**(
[EventHttpRequest](class.eventhttprequest.md) `$req` , int `$type` ,
string `$uri`): bool

Робить HTTP-запит із зазначеного з'єднання. `type` одна з констант
`EventHttpRequest::CMD_*` .

### Список параметрів

`req`
Об'єкт підключення, через який надсилається запит.

`type`
одна з констант
[`EventHttpRequest::CMD_*`](class.eventhttprequest.md#eventhttprequest.constants)
.

`uri`
URI, пов'язаний із запитом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання
**EventHttpConnection::makeRequest()****

` <?phpfunction _request_handler($req, $base) {   echo __FUNCTION__, PHP_EOL; if (is_null($req)) {        echo "Час вийшло
";  |                                             
";         } elseif ($response_code != 200) {             echo "Несподівана відповідь: $response_code
";        } else {            echo "Успішно: $response_code
";             $buf = $req->getInputBuffer();            echo "Тіло відповіді:
";            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {                echo $s, PHP_EOL;            }        }    }    $base->exit(NULL);}$address = "127.0.0.1";$port = 80;$base = new EventBase();$conn = new EventHttpConnection($base, NULL, $address, $port);$conn->setTimeout(5);$req = new EventHttpRequest("_ );$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);$conn->ma req, EventHttpRequest::CMD_GET, "/index.cphp");$base->loop();?> `

Результатом виконання цього прикладу буде щось подібне:

_request_handler
Success: 200
Body:
PHP, date:
2013-03-13T20:27:52+05:00

### Дивіться також

- [EventHttpRequest::addHeader()](eventhttprequest.addheader.md) -
Додає заголовок HTTP до заголовків запиту
