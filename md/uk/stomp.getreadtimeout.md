Повертає час максимального очікування операції читання

-   [« Stomp::error](stomp.error.html)
    
-   [Stomp::getSessionId »](stomp.getsessionid.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Повертає час максимального очікування операції читання
    

# Stomp::getReadTimeout

# stompgetreadtimeout

(PECL stomp >= 0.3.0)

Stomp::getReadTimeout -- stompgetreadtimeout — Повертає час максимального очікування операції читання

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

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.html)

### Значення, що повертаються

Повертає масив із 2 елементами: sec та usec.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

/* подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка соединения: ' . $e->getMessage());
}

var_dump($stomp->getReadTimeout());

/* закрытие соединения */
unset($stomp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

var_dump(stomp_get_read_timeout($link));

/* закрытие соединения */
stomp_close($link);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(2) {
  ["sec"]=>
  int(2)
  ["usec"]=>
  int(0)
}
```