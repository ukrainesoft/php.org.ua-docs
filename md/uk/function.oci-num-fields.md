---
navigation:
  - function.oci-new-descriptor.md: « oci\_new\_descriptor
  - function.oci-num-rows.md: oci\_num\_rows »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_num\_fields

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_num\_fields — Повертає кількість полів через запит

### Опис

```methodsynopsis
oci_num_fields(resource $statement): int
```

Отримує кількість стовпців у запиті, заданому в `statement`

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

### Значення, що повертаються

Повертає кількість порушених рядків у вигляді цілого числа (int).

### Приклади

**Пример #1 Пример использования**oci\_num\_fields()\*\*\*\*

```php
<?php

// Создате таблицу:
//   CREATE TABLE mytab (id NUMBER, quantity NUMBER);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid, OCI_DESCRIBE_ONLY); // используйте OCI_DESCRIBE_ONLY, если не получаете данных

$ncols = oci_num_fields($stid);
for ($i = 1; $i <= $ncols; $i++) {
    echo oci_field_name($stid, $i) . " " . oci_field_type($stid, $i) . "<br>\n";
}

// Выведет:
//    ID NUMBER
//    QUANTITY NUMBER

oci_free_statement($stid);
oci_close($conn);

?>
```
