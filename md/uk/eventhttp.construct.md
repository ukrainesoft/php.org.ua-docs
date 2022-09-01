---
navigation:
  - eventhttp.bind.md: '« EventHttp::bind'
  - eventhttp.removeserveralias.md: 'EventHttp::removeServerAlias »'
  - index.md: PHP Manual
  - class.eventhttp.md: EventHttp
title: 'EventHttp::construct'
---
# EventHttp::construct

(PECL event >= 1.2.6-beta)

EventHttp::construct — Створює об'єкт EventHttp (сервер HTTP)

### Опис

```methodsynopsis
public
   EventHttp::__construct(
    EventBase
     $base
   , 
    EventSslContext
     $ctx
     = null
   )
```

Створює об'єкт сервера HTTP.

### Список параметрів

`base`

Пов'язана основа подій.

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.md). Перетворює простий HTTP-сервер на сервер HTTPS. Це означає, що якщо `ctx` настроєно правильно, то основні події буфера будуть засновані на сокетах OpenSSL. Таким чином, весь трафік проходитиме через SSL або TLS.

> **Зауваження**
> 
> Цей параметр доступний, лише якщо `Event` скомпільований за допомогою OpenSSL і тільки з `Libevent 2.1.0-alpha` і вище.

### Значення, що повертаються

Повертає об'єкт [EventHttp](class.eventhttp.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL event 1.9.0 | Додана підтримка OpenSSL (`ctx` |

### Приклади

**Приклад #1 Простий HTTP-сервер**

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
 * Будет выведено:
 * a=12
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 *
 * $ nc -t 127.0.0.1 8010
 * GET /dump HTTP/1.0
 * Content-Type: text/plain
 * Content-Encoding: UTF-8
 * Connection: close
 * (press Enter)
 *
 * Будет выведено:
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 * (press Enter)
 *
 * $ nc -t 127.0.0.1 8010
 * GET /unknown HTTP/1.0
 * Connection: close
 *
 * Будет выведено:
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
    echo "Команда:", $req->getCommand(), PHP_EOL;
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

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close
(press Enter)

HTTP/1.0 200 OK
Content-Type: text/html; charset=ISO-8859-1
Connection: close
```
