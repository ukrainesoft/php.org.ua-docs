---
navigation:
  - stomp.destruct.md: '« Stomp::destruct'
  - stomp.getreadtimeout.md: 'Stomp::getReadTimeout »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::error'
---
# Stomp::error

# stomperror

(PECL stomp >= 0.1.0)

Stomp :: error -- stomperror — Повертає останню помилку Stomp

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::error(): string
```

Процедурний стиль:

```methodsynopsis
stomp_error(resource $link): string
```

Повертає останню помилку Stomp.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.md)

### Значення, що повертаються

Повертає текст помилки або **`false`** у разі виникнення помилки.

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

var_dump($stomp->error());

if (!$stomp->abort('unknown-transaction', array('receipt' => 'foo'))) {
    var_dump($stomp->error());
}

/* Закрытие соединения */
unset($stomp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
string(43) "Invalid transaction id: unknown-transaction"
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

var_dump(stomp_error($link));

if (!stomp_abort($link, 'unknown-transaction', array('receipt' => 'foo'))) {
    var_dump(stomp_error($link));
}

/* закрытие соединения */
stomp_close($link);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
string(43) "Invalid transaction id: unknown-transaction"
```
