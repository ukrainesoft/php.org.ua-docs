---
navigation:
  - function.oci-field-size.md: « oci\_field\_size
  - function.oci-field-type.md: oci\_field\_type »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_type\_raw
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_type\_raw

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_type\_raw — Повертає вихідний тип поля Oracle

### Опис

```methodsynopsis
oci_field_type_raw(resource $statement, string|int $column): int|false
```

Повертає тип "SQLT" Oracle поля `column`

Якщо ви бажаєте отримати тип поля, то [oci\_field\_type()](function.oci-field-type.md) підійде вам більше.

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає вихідний тип Oracle у вигляді числа або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**oci\_field\_type\_raw()\*\*\*\*

```php
<?php

// Создать таблицу:
//   CREATE TABLE mytab (number_col NUMBER, varchar2_col varchar2(1), clob_col CLOB, date_col DATE);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, 'select * from mytab');
oci_execute($stid, OCI_DESCRIBE_ONLY);  // используйте OCI_DESCRIBE_ONLY, если не получаете данных
$n = oci_num_fields($stid);
for ($i = 1; $i <= $n; ++$i) {
    echo oci_field_name($stid, $i) . " - исходный тип: " . oci_field_type_raw($stid, $i) . "<br>\n";
}

// Выведет:
//    NUMBER_COL - исходный тип: 2
//    VARCHAR2_COL - исходный тип: 1
//    CLOB_COL - исходный тип: 112
//    DATE_COL - исходный тип: 12

oci_free_statement($stid);
oci_close($conn);

?>
```
