---
navigation:
  - eventhttpconnection.makerequest.md: '« EventHttpConnection::makeRequest'
  - eventhttpconnection.setlocaladdress.md: 'EventHttpConnection::setLocalAddress »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::setCloseCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpConnection::setCloseCallback

(PECL event >= 1.8.0)

EventHttpConnection::setCloseCallback — Встановлює callback-функцію при закритті з'єднання

### Опис

```methodsynopsis
public
   EventHttpConnection::setCloseCallback(
    callable
     $callback
   , 
    mixed
     $data
    = ?): void
```

Встановлює callback-функцію при закритті з'єднання.

### Список параметрів

`callback`

Встановлює callback-функцію при закритті з'єднання, яка повинна відповідати прототипу:

```methodsynopsis
callback(
       EventHttpConnection
        $conn
        = null
      , 
       mixed
        $arg
        = null
      ): void
```

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** EventHttpConnection::setCloseCallback()\*\*\*\*

```php
<?php
/*
 * Устанавливаем callback-функцию, при закрытии соединения
 *
 * Скрипт обрабатывает закрытые соединения, используя HTTP API.
 *
 * Использование:
 * 1) Запустите сервер:
 * $ php examples/http_closecb.php 4242
 *
 * 2) Запустите клиента в другом терминале. Наподобие Telnet
 * Сессия должна выглядеть следующим образом:
 *
 * $ nc -t 127.0.0.1 4242
 * GET / HTTP/1.0
 * Connection: close
 *
 * Сервер выведет что-то похожее на следующее:
 *
 * HTTP/1.0 200 OK
 * Content-Type: multipart/x-mixed-replace;boundary=boundarydonotcross
 * Connection: close
 *
 * <html>
 *
 * 3) Завершите соединение с клиентом внезапно,
 * то есть завершите процесс, или просто нажмите Ctrl-C
 *
 * 4) Проверьте, вызывается ли _close_callback.
 * Скрипт должен вывести строку "_close_callback" стандартным выводом.
 *
 * 5) Проверьте, не имеет ли процесс сервера потерянных соединений,
 * наПриклад с утилитой `lsof`.
 */

function _close_callback($conn)
{
    echo __FUNCTION__, PHP_EOL;
}

function _http_default($req, $dummy)
{
    $conn = $req->getConnection();
    $conn->setCloseCallback('_close_callback', NULL);

    /*
    Включив Event::READ, мы защищаем сервер от незакрытых соединений.
    Это особенность Libevent. Библиотека отключает события Event::READ для текущего соединения
    и сервер не уведомляется о разорванных соединениях.

    Таким образом, каждый раз, когда клиент прерывает соединение, мы получаем потерянное соединение.
    НаПриклад, следующее является частью `lsof -p $PID | grep TCP` после того,
    как клиент разорвал соединение:

    57-php     15057 ruslan  6u  unix 0xffff8802fb59c780   0t0  125187 socket
    58:php     15057 ruslan  7u  IPv4             125189   0t0     TCP *:4242 (LISTEN)
    59:php     15057 ruslan  8u  IPv4             124342   0t0     TCP localhost:4242->localhost:37375 (CLOSE_WAIT)

    где $PID – наш ID процесса.

    Следующий блок кода исправляет такие потерянные соединения.
     */
    $bev = $req->getBufferEvent();
    $bev->enable(Event::READ);
    // Мы должны явно это освободить. Смотрите
```

[EventHttpRequest::getConnection()](eventhttprequest.getconnection.md)

```php
$bev->free(); // освобождаем

    $req->addHeader(
        'Content-Type',
        'multipart/x-mixed-replace;boundary=boundarydonotcross',
        EventHttpRequest::OUTPUT_HEADER
    );

    $buf = new EventBuffer();
    $buf->add('<html>');

    $req->sendReply(200, "OK");
    $req->sendReplyChunk($buf);
}

$port = 4242;
if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$base = new EventBase();
$http = new EventHttp($base);

$http->setDefaultCallback("_http_default", NULL);
$http->bind("0.0.0.0", $port);
$base->loop();

?>
```
