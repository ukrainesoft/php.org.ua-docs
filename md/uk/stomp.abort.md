---
navigation:
  - class.stomp.md: « Stomp
  - stomp.ack.md: 'Stomp::ack »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::abort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::abort

# stomp\_abort

(PECL stomp >= 0.1.0)

Stomp::abort -- stomp\_abort — Скасує виконання поточної транзакції

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::abort(string $transaction_id, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_abort(resource $link, string $transaction_id, array $headers = ?): bool
```

Скасує виконання поточної транзакції.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`transaction_id`

Транзакція, яку слід перервати.

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

/* подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка соединения: ' . $e->getMessage());
}

/* начало транзакции */
$stomp->begin('t1');

/* отправка сообщения в очередь */
$stomp->send('/queue/foo', 'bar', array('transaction' => 't1'));

/* откат транзакции */
$stomp->abort('t1');

/* разрыв подключения */
unset($stomp);
?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* подключение */
$link = stomp_connect('tcp://localhost:61613');

/* проверка подключения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

/* начало транзакции */
stomp_begin($link, 't1');

/* отправка сообщения в очередь 'foo' */
stomp_send($link, '/queue/foo', 'bar', array('transaction' => 't1'));

/* откат транзакции */
stomp_abort($link, 't1');

/* разрыв подключения */
stomp_close($link);

?>
```

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.
