---
navigation:
  - function.oci-fetch.md: « oci\_fetch
  - function.oci-field-name.md: oci\_field\_name »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_field\_is\_null
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_field\_is\_null

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_field\_is\_null — Перевіряє, чи поле у ​​поточному отриманому рядку дорівнює **`null`**

### Опис

```methodsynopsis
oci_field_is_null(resource $statement, string|int $column): bool
```

Перевіряє, чи є значення, передане в поле `column`из текущего ряда`statement` рівним **`null`**

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

`column`

Може бути порядковий номер поля (з 1) або ім'я поля.

### Значення, що повертаються

Повертає **`true`**, якщо `column`равен\*\*`null`**, и**`false`\*\* якщо ні.

### Приклади

**Приклад #1 Приклад использования[oci\_field\_name()](function.oci-field-name.md)**

```php
<?php

// Создайте таблицу:
//   CREATE TABLE mytab (c1 NUMBER);
//   INSERT INTO mytab VALUES (1);
//   INSERT INTO mytab VALUES (NULL);

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_RETURN_NULLS)) != false) {
    $ncols = oci_num_fields($stid);
    for ($col = 1; $col <= $ncols; $col++) {
        var_dump(oci_field_is_null($stid, $col));
    }
}

// Выведет:
//    bool(false)
//    bool(true)

oci_free_statement($stid);
oci_close($conn);

?>
```
