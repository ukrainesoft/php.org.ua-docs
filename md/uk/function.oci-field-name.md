---
navigation:
  - function.oci-field-is-null.md: « oci\_field\_is\_null
  - function.oci-field-precision.md: oci\_field\_precision »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_name

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_name — Повертає ім'я поля з результату запиту

### Опис

```methodsynopsis
oci_field_name(resource $statement, string|int $column): string|false
```

Повертає ім'я поля `column`из результата запроса.

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає ім'я у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** oci\_field\_name()\*\*\*\*

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
echo "<th>Name</th>";
echo "<th>Type</th>";
echo "<th>Length</th>";
echo "</tr>\n";

$ncols = oci_num_fields($stid);

for ($i = 1; $i <= $ncols; $i++) {
    $column_name  = oci_field_name($stid, $i);
    $column_type  = oci_field_type($stid, $i);

    echo "<tr>";
    echo "<td>$column_name</td>";
    echo "<td>$column_type</td>";
    echo "</tr>\n";
}

echo "</table>\n";

// Выведет:
//    Name           Type
//    NUMBER_COL    NUMBER
//    VARCHAR2_COL  VARCHAR2
//    CLOB_COL      CLOB
//    DATE_COL      DATE

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [oci\_num\_fields()](function.oci-num-fields.md) \- Повертає кількість полів у результаті запиту
-   [oci\_field\_type()](function.oci-field-type.md) \- Повертає ім'я типу поля
-   [oci\_field\_size()](function.oci-field-size.md) \- Повертає розмір поля
