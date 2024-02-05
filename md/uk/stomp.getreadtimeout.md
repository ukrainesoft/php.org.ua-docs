---
navigation:
  - stomp.error.md: '« Stomp::error'
  - stomp.getsessionid.md: 'Stomp::getSessionId »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::getReadTimeout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::getReadTimeout

# stomp\_get\_read\_timeout

(PECL stomp >= 0.3.0)

Stomp::getReadTimeout -- stomp\_get\_read\_timeout — Повертає час максимального очікування операції читання

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::getReadTimeout(): array
```

Процедурний стиль:

```methodsynopsis
stomp_get_read_timeout(resource $link): array
```

Повертає час максимального очікування операції читання

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

### Значення, що повертаються

Повертає масив із 2 елементами: sec та usec.

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

var_dump($stomp->getReadTimeout());

/* закрытие соединения */
unset($stomp);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["sec"]=>
  int(2)
  ["usec"]=>
  int(0)
}
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

var_dump(stomp_get_read_timeout($link));

/* закрытие соединения */
stomp_close($link);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["sec"]=>
  int(2)
  ["usec"]=>
  int(0)
}
```
