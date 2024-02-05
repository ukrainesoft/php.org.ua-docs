---
navigation:
  - stomp.abort.md: '« Stomp::abort'
  - stomp.begin.md: 'Stomp::begin »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::ack'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::ack

# stomp\_ack

(PECL stomp >= 0.1.0)

Stomp::ack -- stomp\_ack — Підтверджує отримання повідомлення

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::ack(mixed $msg, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_ack(resource $link, mixed $msg, array $headers = ?): bool
```

Підтверджує факт отримання повідомлення із черги, використовуючи підтвердження клієнта.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`msg`

Повідомлення/ідентифікатор повідомлення, отримання якого має бути підтверджено.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка соединения: ' . $e->getMessage());
}

/* отправка сообщения в очередь 'foo' */
$stomp->send($queue, $msg);

/* подписка на сообщения из очереди 'foo' */
$stomp->subscribe($queue);

/* чтение фрейма */
$frame = $stomp->readFrame();

if ($frame->body === $msg) {
    /* подтверждение получения фрейма */
    $stomp->ack($frame);
}

/* отмена подписки к очереди */
$stomp->unsubscribe($queue);

/* закрытие подключения */
unset($stomp);

?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

/* начало транзакции */
stomp_begin($link, 't1');

/* отправка сообщения в очередь  'foo' */
stomp_send($link, $queue, $msg, array('transaction' => 't1'));

/* подтверждение транзакции */
stomp_commit($link, 't1');

/* подписка на сообщения из очереди 'foo' */
stomp_subscribe($link, $queue);

/* чтение фрейма */
$frame = stomp_read_frame($link);

if ($frame['body'] === $msg) {
    /* подтверждение получения фрейма */
    stomp_ack($link, $frame['headers']['message-id']);
}

/* отмена подписки к очереди */
stomp_unsubscribe($link, $queue);

/* закрытие подключения */
stomp_close($link);

?>
```

### Примітки

> **Зауваження** :
> 
> Також може бути зазначений заголовок транзакції, що означає, що прийом повідомлення повинен бути частиною іменованої транзакції.

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.
