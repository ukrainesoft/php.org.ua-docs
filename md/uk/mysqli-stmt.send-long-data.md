Надсилання даних блоками

-   [« mysqlistmt::resultmetadata](mysqli-stmt.result-metadata.html)
    
-   [mysqlistmt::$sqlstate »](mysqli-stmt.sqlstate.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Надсилання даних блоками
    

# mysqlistmt::sendlongdata

# mysqlistmtsendlongdata

(PHP 5, PHP 7, PHP 8)

mysqlistmt::sendlongdata - mysqlistmtsendlongdata — Надсилання даних блоками

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::send_long_data(int $param_num, string $data): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_send_long_data(mysqli_stmt $statement, int $param_num, string $data): bool
```

Дозволяє пересилати дані параметра на сервер частинами (або чанками), наприклад коли розмір великого об'єкта (blob) перевищує `max_allowed_packet`. Цю функцію можна запускати багаторазово, щоб надіслати частини символьних або двійкових даних стовпця. Дані у стовпці повинні мати тип TEXT або BLOB.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

`param_num`

Вказує, із яким параметром пов'язані дані. Параметри нумеруються з нуля.

`data`

Рядок, що містить дані, що пересилаються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$stmt = $mysqli->prepare("INSERT INTO messages (message) VALUES (?)");
$null = NULL;
$stmt->bind_param("b", $null);
$fp = fopen("messages.txt", "r");
while (!feof($fp)) {
    $stmt->send_long_data(0, fread($fp, 8192));
}
fclose($fp);
$stmt->execute();
?>
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.md) - готує SQL вираз до виконання
-   [mysqlistmtbindparam()](mysqli-stmt.bind-param.html) - Прив'язка змінних до параметрів запиту, що готується.