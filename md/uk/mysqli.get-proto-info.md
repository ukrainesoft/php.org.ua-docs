Повертає версію використовуваного MySQL протоколу

-   [« mysqli::$host\_info](mysqli.get-host-info.html)
    
-   [mysqli::$server\_info »](mysqli.get-server-info.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає версію використовуваного MySQL протоколу
    

# mysqli::$protocolversion

# mysqligetprotoinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$protocolversion -- mysqligetprotoinfo — Повертає версію протоколу, що використовується MySQL

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->protocol\_version](mysqli.get-proto-info.html)

Процедурний стиль

```methodsynopsis
mysqli_get_proto_info(mysqli $mysql): int
```

Повертає ціле число, що є версією протоколу MySQL, використовуваного для з'єднання, переданого в `mysql`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Повертає ціле число, яке представляє версію протоколу.

### Приклади

**Приклад #1 Приклад використання $mysqli->protocolversion**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* Вывести версию протокола */
printf("Версия протокола: %d\n", $mysqli->protocol_version);

/* Закрыть соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password");

/* Проверить соединение */
if (mysqli_connect_errno()) {
    printf("Подключение не удалось: %s\n", mysqli_connect_error());
    exit();
}

/* Вывести версию протокола */
printf("Версия протокола: %d\n", mysqli_get_proto_info($link));

/* Закрыть соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Protocol version: 10
```

### Дивіться також

-   [mysqli\_get\_host\_info()](mysqli.get-host-info.html) - Повертає рядок, що містить тип використовуваної сполуки