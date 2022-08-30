Повертає ідентифікатор поточної сесії Stomp

-   [« Stomp::getReadTimeout](stomp.getreadtimeout.html)
    
-   [Stomp::hasFrame »](stomp.hasframe.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Повертає ідентифікатор поточної сесії Stomp
    

# Stomp::getSessionId

# stompgetsessionід

(PECL stomp >= 0.1.0)

Stomp::getSessionId -- stompgetsessionid — Повертає ідентифікатор поточної сесії Stomp

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::getSessionId(): string|false
```

Процедурний стиль:

```methodsynopsis
stomp_get_session_id(resource $link): string|false
```

Повертає ідентифікатор сесії Stomp.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stompconnect()](stomp.construct.html)

### Значення, що повертаються

Ідентифікатор сесії (string) у разі успішного виконання або **`false`** у разі виникнення помилки.

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

var_dump($stomp->getSessionId());

/* закрытие подключения */
unset($stomp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(35) "ID:php.net-52873-1257291895530-4:14"
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

var_dump(stomp_get_session_id($link));

/* закрытие подключения */
stomp_close($link);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(35) "ID:php.net-52873-1257291895530-4:14"
```