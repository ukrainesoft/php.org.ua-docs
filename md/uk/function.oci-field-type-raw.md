---
navigation:
  - function.oci-field-size.html: « ocifieldsize
  - function.oci-field-type.html: ocifieldtype »
  - index.html: PHP Manual
  - ref.oci8.html: OCI8 Функции
title: ocifieldtyperaw
---
# ocifieldtyperaw

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifieldtyperaw — Повертає вихідний тип поля Oracle

### Опис

```methodsynopsis
oci_field_type_raw(resource $statement, string|int $column): int|false
```

Повертає тип "SQLT" Oracle поля `column`

Якщо ви бажаєте отримати тип поля, то [ocifieldtype()](function.oci-field-type.html) підійде вам більше.

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає вихідний тип Oracle у вигляді числа або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocifieldtyperaw()****

```php
<?php

// Создать таблицу:
//   CREATE TABLE mytab (number_col NUMBER, varchar2_col varchar2(1), clob_col CLOB, date_col DATE);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, 'select * from mytab');
oci_execute($stid, OCI_DESCRIBE_ONLY);  // используйте OCI_DESCRIBE_ONLY, если не получаете данных
$n = oci_num_fields($stid);
for ($i = 1; $i <= $n; ++$i) {
    echo oci_field_name($stid, $i) . " - исходный тип: " . oci_field_type_raw($stid, $i) . "<br>\n";
}

// Выведет:
//    NUMBER_COL - исходный тип: 2
//    VARCHAR2_COL - исходный тип: 1
//    CLOB_COL - исходный тип: 112
//    DATE_COL - исходный тип: 12

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocicolumntyperaw()](function.ocicolumntyperaw.html). У PHP 5.0.0 і вище [ocicolumntyperaw()](function.ocicolumntyperaw.html) є аліасом \*\*ocifieldtyperaw()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
