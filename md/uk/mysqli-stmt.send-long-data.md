---
navigation:
  - mysqli-stmt.result-metadata.md: '« mysqli\_stmt::result\_metadata'
  - mysqli-stmt.sqlstate.md: 'mysqli\_stmt::$sqlstate »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::send\_long\_data'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::send\_long\_data

# mysqli\_stmt\_send\_long\_data

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::send\_long\_data -- mysqli\_stmt\_send\_long\_data — Надсилання даних блоками

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

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`param_num`

Вказує, із яким параметром пов'язані дані. Параметри нумеруються з нуля.

`data`

Рядок, що містить дані, що пересилаються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$stmt = $mysqli->prepare("INSERT INTO messages (message) VALUES (?)");
$null = NULL;
$stmt->bind_param("b", $null);
$fp = fopen("messages.txt", "r");
while (!feof($fp)) {
    $stmt->send_long_data(0, fread($fp, 8192));
}
fclose($fp);
$stmt->execute();
?>
```

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
