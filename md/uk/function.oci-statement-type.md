---
navigation:
  - function.oci-set-prefetch.md: « oci\_set\_prefetch
  - function.oci-unregister-taf-callback.md: oci\_unregister\_taf\_callback »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_statement\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_statement\_type

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_statement\_type — Повертає тип виразу

### Опис

```methodsynopsis
oci_statement_type(resource $statement): string|false
```

Повертає вираз, що відповідає одному з типів параметра `statement`OCI8.

### Список параметрів

`statement`

Допустимий ідентифікатор оператора OCI8, який повертається [oci\_parse()](function.oci-parse.md)

### Значення, що повертаються

Возвращает тип параметра`statement`, який може бути одним з нижченаведених значень:

**Тип оператора**

| Возвращаемое значение | Примечание |
| --- | --- |
| `ALTER` |  |
| `BEGIN` |  |
| `CALL` |  |
| `CREATE` |  |
| `DECLARE` |  |
| `DELETE` |  |
| `DROP` |  |
| `INSERT` |  |
| `SELECT` |  |
| `UPDATE` |  |
| `UNKNOWN` |  |

Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**oci\_statement\_type()\*\*\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'DELETE FROM departments WHERE department_id = 130;');
if (oci_statement_type($stid) == "DELETE") {
    trigger_error('Вы не имеете прав для удаления записей из таблицы', E_USER_ERROR);
}
else {
    oci_execute($stid);  // удалить запись
}

oci_free_statement($stid);
oci_close($conn);

?>
```
