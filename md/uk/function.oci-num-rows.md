---
navigation:
  - function.oci-num-fields.md: « oci\_num\_fields
  - function.oci-parse.md: oci\_parse »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_num\_rows

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_num\_rows — Повертає кількість рядків, змінених під час виконання запиту

### Опис

```methodsynopsis
oci_num_rows(resource $statement): int|false
```

Повертає кількість рядків, які торкнулися в процесі виконання запиту.

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

### Значення, що повертаються

Повертає число порушених рядків у вигляді integer або \*\*`false`\*\*в случае возникновения ошибки

### Приклади

**Пример #1 Пример использования**oci\_num\_rows()\*\*\*\*

```php
<?php

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "create table emp2 as select * from employees");
oci_execute($stid);
echo oci_num_rows($stid) . " строк вставлено.<br />\n";
oci_free_statement($stid);

$stid = oci_parse($conn, "delete from emp2");
oci_execute($stid, OCI_DEFAULT);
echo oci_num_rows($stid) . " строк удалено.<br />\n";
oci_commit($conn);
oci_free_statement($stid);

$stid = oci_parse($conn, "drop table emp2");
oci_execute($stid);
oci_free_statement($stid);

oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Функция*не* повертає кількість рядків у результаті виразу SELECT! Для запитів SELECT **oci\_num\_rows()** поверне кількість рядків, які були прочитані в буфер за допомогою функцій **oci\_fetch\*()**
