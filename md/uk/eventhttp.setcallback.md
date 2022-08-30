Встановлює callback-функцію для вказаного URI

-   [« EventHttp::setAllowedMethods](eventhttp.setallowedmethods.md)
    
-   [EventHttp::setDefaultCallback »](eventhttp.setdefaultcallback.md)
    
-   [PHP Manual](index.md)
    
-   [EventHttp](class.eventhttp.md)
    
-   Встановлює callback-функцію для вказаного URI
    

# EventHttp::setCallback

(PECL event >= 1.4.0-beta)

EventHttp::setCallback — Встановлює callback-функцію для вказаного URI

### Опис

```methodsynopsis
public
   EventHttp::setCallback(
    string
     $path
   , 
    string
     $cb
   , 
    string
     $arg
    = ?): void
```

Встановлює callback-функцію для зазначеного URI.

### Список параметрів

`path`

Шлях для виклику callback-функції.

`cb`

Callback-функція [callable](language.types.callable.md), яка викликається за запитаним `path`. Повинна відповідати наступному прототипу:

```methodsynopsis
callback(
       EventHttpRequest
        $req
        = NULL
      , 
       mixed
        $arg
        = NULL
      ): void
```

`req`

Об'єкт [EventHttpRequest](class.eventhttprequest.md)

`arg`

Дані користувача.

`arg`

Дані користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventHttp::setCallback()****

```php
<?php
/*
 * Простой HTTP-сервер.
 *
 * Чтобы проверить:
 * 1) Запустите его на выбранном вами порту, например:
 * $ php examples/http.php 8010
 * 2) В другом терминале подключитесь к какому-либо адресу на этом порту
 * и сделайте запрос GET или POST (другие здесь отключены), например:
 * $ nc -t 127.0.0.1 8010
 * POST /about HTTP/1.0
 * Content-Type: text/plain
 * Content-Length: 4
 * Connection: close
 * (press Enter)
 *
 * Будет выводено
 * a=12
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 *
 * 3) Посмотрите, что сервер выводит в предыдущем окне терминала.
 */

function _http_dump($req, $data) {
    static $counter      = 0;
    static $max_requests = 2;

    if (++$counter >= $max_requests)  {
        echo "Счётчик достиг максимальных запросов $max_requests. Выходим\n";
        exit();
    }

    echo __METHOD__, " called\n";
    echo "запрос:"; var_dump($req);
    echo "данные:"; var_dump($data);

    echo "\n===== DUMP =====\n";
    echo "команда:", $req->getCommand(), PHP_EOL;
    echo "URI:", $req->getUri(), PHP_EOL;
    echo "Заголовки ввода:"; var_dump($req->getInputHeaders());
    echo "Выходные заголовки:"; var_dump($req->getOutputHeaders());

    echo "\n >> Отправка ответа ...";
    $req->sendReply(200, "OK");
    echo "OK\n";

    echo "\n >> Чтение входного буфера ...\n";
    $buf = $req->getInputBuffer();
    while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
        echo $s, PHP_EOL;
    }
    echo "Нет больше данных в буфере\n";
}

function _http_about($req) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Отправка ответа ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

function _http_default($req, $data) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Отправка ответа ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

$port = 8010;
if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Неверный порт");
}

$base = new EventBase();
$http = new EventHttp($base);
$http->setAllowedMethods(EventHttpRequest::CMD_GET | EventHttpRequest::CMD_POST);

$http->setCallback("/dump", "_http_dump", array(4, 8));
$http->setCallback("/about", "_http_about");
$http->setDefaultCallback("_http_default", "пользовательские данные");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
a=12
HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close
```

### Дивіться також

-   [EventHttp::setDefaultCallback()](eventhttp.setdefaultcallback.md) - Встановлює callback-функцію за промовчанням для обробки запитів, які не перехоплюються конкретними callback-функціями