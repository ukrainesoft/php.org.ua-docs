---
navigation:
  - function.oci-field-precision.html: « ocifieldprecision
  - function.oci-field-size.html: ocifieldsize »
  - index.html: PHP Manual
  - ref.oci8.html: OCI8 Функции
title: ocifieldscale
---
# ocifieldscale

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifieldscale — Повертає масштаб поля

### Опис

```methodsynopsis
oci_field_scale(resource $statement, string|int $column): int|false
```

Повертає масштаб поля під номером `column`

Для полів типу FLOAT точність, що отримується за допомогою [ocifieldprecision()](function.oci-field-precision.html)більше нуля, а масштаб дорівнює -127. Якщо точність поля дорівнює нулю, тип поля - NUMBER. Інакше, тип поля може бути описаний як NUMBER(precision, scale).

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути номер поля (нумерація починається з 1) або ім'ям.

### Значення, що повертаються

Повертає масштаб у вигляді числа або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **ocifieldscale()** Example**

```php
<?php

// Создайте таблицу:
//   CREATE TABLE mytab (c1 NUMBER, c2 FLOAT, c3 NUMBER(4), c4 NUMBER(5,3));

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid, OCI_DESCRIBE_ONLY); // используйте OCI_DESCRIBE_ONLY, если не получаете данных

$ncols = oci_num_fields($stid);
for ($i = 1; $i <= $ncols; $i++) {
    echo oci_field_name($stid, $i) . " "
        . oci_field_precision($stid, $i) . " "
        . oci_field_scale($stid, $i) . "<br>\n";
}

// Выведет:
//   C1    0 -127
//   C2  126 -127
//   C3    4    0
//   C4    5    3

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocicolumnscale()](function.ocicolumnscale.html). У PHP 5.0.0 і вище [ocicolumnscale()](function.ocicolumnscale.html) є аліасом \*\*ocifieldscale()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.

### Дивіться також

-   [ocifieldprecision()](function.oci-field-precision.html) - Повертає точність поля
-   [ocifieldtype()](function.oci-field-type.html) - Повертає ім'я типу поля
