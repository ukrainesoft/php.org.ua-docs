---
navigation:
  - function.oci-set-prefetch.html: « ocisetprefetch
  - function.oci-unregister-taf-callback.html: ociunregistertafcallback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocistatementtype
---
# ocistatementtype

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocistatementtype — Повертає тип виразу

### Опис

```methodsynopsis
oci_statement_type(resource $statement): string|false
```

Повертає вираз, що відповідає одному з типів параметра `statement` OCI8.

### Список параметрів

`statement`

Допустимий ідентифікатор оператора OCI8, який повертається [ociparse()](function.oci-parse.md)

### Значення, що повертаються

Повертає тип параметра `statement`, який може бути одним з нижченаведених значень:

**Тип оператора**

| Возвращаемое значение | Примечание |
| --- | --- |
| `ALTER` |  |
| `BEGIN` |  |
| `CALL` | Подано в PHP 5.2.1 (PECL OCI8 1.2.3) |
| `CREATE` |  |
| `DECLARE` |  |
| `DELETE` |  |
| `DROP` |  |
| `INSERT` |  |
| `SELECT` |  |
| `UPDATE` |  |
| `UNKNOWN` |  |

Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocistatementtype()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'DELETE FROM departments WHERE department_id = 130;');
if (oci_statement_type($stid) == "DELETE") {
    trigger_error('Вы не имеете прав для удаления записей из таблицы', E_USER_ERROR);
}
else {
    oci_execute($stid);  // удалить запись
}

oci_free_statement($stid);
oci_close($conn);

?>
```
