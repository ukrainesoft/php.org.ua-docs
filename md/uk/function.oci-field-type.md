---
navigation:
  - function.oci-field-type-raw.md: « oci\_field\_type\_raw
  - function.oci-free-descriptor.md: oci\_free\_descriptor »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_type

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_type — Повертає назву типу поля

### Опис

```methodsynopsis
oci_field_type(resource $statement, string|int $column): string|int|false
```

Повертає назву типу поля.

### Список параметрів

`statement`

Допустимий ідентифікатор OCI-виразу.

`column`

Може бути задано індексом (починаючи з 1) або на ім'я.

### Значення, що повертаються

Повертає тип поля як рядок (string) або ціле число (int) або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**oci\_field\_type()\*\*\*\*

```php
<?php

// Создайте таблицу:
//   CREATE TABLE mytab (number_col NUMBER, varchar2_col varchar2(1),
//                       clob_col CLOB, date_col DATE);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid, OCI_DESCRIBE_ONLY); // используйте OCI_DESCRIBE_ONLY, если не получаете данных

echo "<table border=\"1\">\n";
echo "<tr>";
echo "<th>Имя</th>";
echo "<th>Тип</th>";
echo "<th>Длина</th>";
echo "</tr>\n";

$ncols = oci_num_fields($stid);

for ($i = 1; $i <= $ncols; $i++) {
    $column_name  = oci_field_name($stid, $i);
    $column_type  = oci_field_type($stid, $i);
    $column_size  = oci_field_size($stid, $i);

    echo "<tr>";
    echo "<td>$column_name</td>";
    echo "<td>$column_type</td>";
    echo "<td>$column_size</td>";
    echo "</tr>\n";
}

echo "</table>\n";

// Выведет:
//    Имя           Тип       Длина
//    NUMBER_COL    NUMBER        22
//    VARCHAR2_COL  VARCHAR2       1
//    CLOB_COL      CLOB        4000
//    DATE_COL      DATE           7

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [oci\_num\_fields()](function.oci-num-fields.md) \- Повертає кількість полів у результаті запиту
-   [oci\_field\_name()](function.oci-field-name.md) \- Повертає ім'я поля з результату запиту
-   [oci\_field\_size()](function.oci-field-size.md) \- Повертає розмір поля
