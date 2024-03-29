---
navigation:
  - function.oci-field-precision.md: « oci\_field\_precision
  - function.oci-field-size.md: oci\_field\_size »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_scale
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_scale

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_scale — Повертає масштаб поля

### Опис

```methodsynopsis
oci_field_scale(resource $statement, string|int $column): int|false
```

Повертає масштаб поля під номером `column`

Для полів типу FLOAT точність, що отримується за допомогою [oci\_field\_precision()](function.oci-field-precision.md)більше нуля, а масштаб дорівнює -127. Якщо точність поля дорівнює нулю, тип поля - NUMBER. Інакше, тип поля може бути описаний як NUMBER(precision, scale).

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає масштаб у вигляді числа або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1**oci\_field\_scale()**Example**

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

-   [oci\_field\_precision()](function.oci-field-precision.md) \- Повертає точність поля
-   [oci\_field\_type()](function.oci-field-type.md) \- Повертає ім'я типу поля
