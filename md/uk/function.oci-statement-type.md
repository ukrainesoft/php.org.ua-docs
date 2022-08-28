Повертає тип виразу

-   [« oci\_set\_prefetch](function.oci-set-prefetch.html)
    
-   [oci\_unregister\_taf\_callback »](function.oci-unregister-taf-callback.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає тип виразу
    

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

Допустимий ідентифікатор оператора OCI8, який повертається [oci\_parse()](function.oci-parse.html)

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