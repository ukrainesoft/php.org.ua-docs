Встановлює граничний час очікування операції читання

-   [« Stomp::send](stomp.send.html)
    
-   [Stomp::subscribe »](stomp.subscribe.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Встановлює граничний час очікування операції читання
    

# Stomp::setReadTimeout

# stompsetreadtimeout

(PECL stomp >= 0.3.0)

Stomp::setReadTimeout -- stompsetreadtimeout — Встановлює граничний час очікування операції читання

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::setReadTimeout(int $seconds, int $microseconds = ?): void
```

Процедурний стиль:

```methodsynopsis
stomp_set_read_timeout(resource $link, int $seconds, int $microseconds = ?): void
```

Встановлює граничний час очікування на операцію читання.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.html)

`seconds`

Секундна частина очікування операції.

`microseconds`

Мікросекундний час очікування операції.

### Значення, що повертаються

Функція не повертає значення після виконання.

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

$stomp->setReadTimeout(10);

/* закрытие подключения */
unset($stomp);

?>
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка подключения: ' . stomp_connect_error());
}

stomp_set_read_timeout($link, 10);

/* закрытие подключения */
stomp_close($link);

?>
```