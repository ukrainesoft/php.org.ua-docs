---
navigation:
  - stomp.resources.md: « Типи ресурсів
  - ref.stomp.md: Функции Stomp »
  - index.md: PHP Manual
  - book.stomp.md: Stomp
title: Приклади
---
# Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* Подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка подключения: ' . $e->getMessage());
}

/* Отправка сообщения в очередь 'foo' */
$stomp->send($queue, $msg);

/* Подписка к сообщениям в очереди 'foo' */
$stomp->subscribe($queue);

/* Чтение фрейма */
$frame = $stomp->readFrame();

if ($frame->body === $msg) {
    var_dump($frame);

    /* отклик, что сообщения было получено */
    $stomp->ack($frame);
}

/* Закрытие соединения */
unset($stomp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(StompFrame)#2 (3) {
  ["command"]=>
  string(7) "MESSAGE"
  ["headers"]=>
  array(5) {
    ["message-id"]=>
    string(41) "ID:php.net-55293-1257226743606-4:2:-1:1:1"
    ["destination"]=>
    string(10) "/queue/foo"
    ["timestamp"]=>
    string(13) "1257226805828"
    ["expires"]=>
    string(1) "0"
    ["priority"]=>
    string(1) "0"
  }
  ["body"]=>
  string(3) "bar"
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* Подключение */
$link = stomp_connect('ssl://localhost:61612');

/* Проверка подключения */
if (!$link) {
    die('Ошибка подключения: ' . stomp_connect_error());
}

/* Начало транзакции */
stomp_begin($link, 't1');

/* Отправка сообщения в очередь 'foo' */
stomp_send($link, $queue, $msg, array('transaction' => 't1'));

/* Выполнение транзакции */
stomp_commit($link, 't1');

/* Подписка к сообщениям в очереди 'foo' */
stomp_subscribe($link, $queue);

/* Чтение фрейма */
$frame = stomp_read_frame($link);

if ($frame['body'] === $msg) {
    var_dump($frame);

    /* отклик, что сообщения было получено */
    stomp_ack($link, $frame['headers']['message-id']);
}

/* Закрытие соединения */
stomp_close($link);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  ["command"]=>
  string(7) "MESSAGE"
  ["body"]=>
  string(3) "bar"
  ["headers"]=>
  array(6) {
    ["transaction"]=>
    string(2) "t1"
    ["message-id"]=>
    string(41) "ID:php.net-55293-1257226743606-4:3:-1:1:1"
    ["destination"]=>
    string(10) "/queue/foo"
    ["timestamp"]=>
    string(13) "1257227037059"
    ["expires"]=>
    string(1) "0"
    ["priority"]=>
    string(1) "0"
  }
}
```
