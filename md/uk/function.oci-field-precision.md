---
navigation:
  - function.oci-field-name.md: « oci\_field\_name
  - function.oci-field-scale.md: oci\_field\_scale »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_precision
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_precision

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_precision — Повертає точність поля

### Опис

```methodsynopsis
oci_field_precision(resource $statement, string|int $column): int|false
```

Повертає точність поля `column`

Для полів типу FLOAT точність більша за нуль, а масштаб дорівнює -127. Якщо точність поля дорівнює нулю, тип поля - NUMBER. Інакше, тип поля може бути описаний як NUMBER(precision, scale).

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає точність у вигляді числа або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**oci\_field\_precision()\*\*\*\*

```php
<?php

// Создайте таблицу:
//   CREATE TABLE mytab (c1 NUMBER, c2 FLOAT, c3 NUMBER(4), c4 NUMBER(5,3));

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid, OCI_DESCRIBE_ONLY); // используйте OCI_DESCRIBE_ONLY, если не получаете данных

$ncols = oci_num_fields($stid);
for ($i = 1; $i <= $ncols; $i++) {
    echo oci_field_name($stid, $i) . " "
        . oci_field_precision($stid, $i) . " "
        . oci_field_scale($stid, $i) . "<br>\n";
}

// Выведет:
//   C1    0 -127
//   C2  126 -127
//   C3    4    0
//   C4    5    3

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [oci\_field\_scale()](function.oci-field-scale.md) \- Повертає масштаб поля
-   [oci\_field\_type()](function.oci-field-type.md) \- Повертає ім'я типу поля
