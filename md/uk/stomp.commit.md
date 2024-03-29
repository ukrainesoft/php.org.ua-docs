---
navigation:
  - stomp.begin.md: '« Stomp::begin'
  - stomp.construct.md: 'Stomp::\_\_construct »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::commit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::commit

# stomp\_commit

(PECL stomp >= 0.1.0)

Stomp::commit -- stomp\_commit — Виконує поточну транзакцію

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::commit(string $transaction_id, array $headers = ?): bool
```

Процедурний стиль:

```methodsynopsis
stomp_commit(resource $link, string $transaction_id, array $headers = ?): bool
```

Виконує поточну транзакцію.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

`transaction_id`

Ідентифікатор транзакції.

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

/* Начало транзакции */
$stomp->begin('t1');

/* отправка сообщения в очередь */
$stomp->send('/queue/foo', 'bar', array('transaction' => 't1'));

/* выполнение транзакции */
$stomp->commit('t1');

/* закрытие подключения */
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

/* Начало транзакции */
stomp_begin($link, 't1');

/* Отправка сообщения в очередь 'foo' */
stomp_send($link, '/queue/foo', 'bar', array('transaction' => 't1'));

/* Выполнение транзакции */
stomp_commit($link, 't1');

/* Закрытие изменения */
stomp_close($link);

?>
```

### Примітки

**Підказка**

Stomp асинхронний за своєю суттю. Синхронний зв'язок може бути реалізований додаванням receipt-заголовка. Це змусить методи нічого не повертати, доки сервер не підтвердить отримання повідомлення або буде перевищено час очікування повідомлення.
