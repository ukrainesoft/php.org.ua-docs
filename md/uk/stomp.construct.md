Відкриває з'єднання

-   [« Stomp::commit](stomp.commit.html)
    
-   [Stomp::destruct »](stomp.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](class.stomp.html)
    
-   Відкриває з'єднання
    

# Stomp::construct

# stompconnect

(PECL stomp >= 0.1.0)

Stomp::construct - stompconnect — Відкриває з'єднання

### Опис

Об'єктно-орієнтований стиль (конструктор):

public **Stomp::construct**  
string `$broker` = iniget("stomp.defaultbrokeruri"),  
string `$username`  
string `$password`  
array `$headers`

Процедурний стиль:

```methodsynopsis
stomp_connect(    string $broker = ini_get("stomp.default_broker_uri"),    string $username = ?,    string $password = ?,    array $headers = ?): resource
```

Відкриває з'єднання до Stomp-сумісного брокера повідомлень (Message Broker).

### Список параметрів

`broker`

URI брокера

`username`

Ім'я користувача

`password`

Пароль

`headers`

Асоціативний масив, який містить додаткові заголовки (приклад: receipt).

### Значення, що повертаються

> **Зауваження**
> 
> Також може бути зазначений заголовок транзакції, що означає, що прийом повідомлення повинен бути частиною іменованої транзакції.

### список змін

| Версия | Описание |
| --- | --- |
| PECL Stomp 1.0.1 | Доданий параметр `headers` |

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

/* закрытие соединения */
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
    die('Ошибка соединения: ' . stomp_connect_error());
}

/* Закрытие соединения */
stomp_close($link);

?>
```