Повертає кількість рядків, змінених у процесі виконання запиту

-   [« oci\_num\_fields](function.oci-num-fields.html)
    
-   [oci\_parse »](function.oci-parse.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає кількість рядків, змінених у процесі виконання запиту
    

# ocinumrows

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinumrows — Повертає кількість рядків, змінених під час виконання запиту

### Опис

```methodsynopsis
oci_num_rows(resource $statement): int|false
```

Повертає кількість рядків, які торкнулися в процесі виконання запиту.

### Список параметрів

`statement`

Ідентифікатор допустимого запиту OCI.

### Значення, що повертаються

Повертає число порушених рядків у вигляді integer або **`false`** у разі виникнення помилки

### Приклади

**Приклад #1 Приклад використання **ocinumrows()****

```php
<?php

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, "create table emp2 as select * from employees");
oci_execute($stid);
echo oci_num_rows($stid) . " строк вставлено.<br />\n";
oci_free_statement($stid);

$stid = oci_parse($conn, "delete from emp2");
oci_execute($stid, OCI_DEFAULT);
echo oci_num_rows($stid) . " строк удалено.<br />\n";
oci_commit($conn);
oci_free_statement($stid);

$stid = oci_parse($conn, "drop table emp2");
oci_execute($stid);
oci_free_statement($stid);

oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Функція *не* повертає кількість рядків у результаті вираження SELECT! Для запитів SELECT **ocinumrows()** поверне кількість рядків, які були прочитані в буфер за допомогою функцій **ocifetch**

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocirowcount()](function.ocirowcount.html). У PHP 5.0.0 і вище [ocirowcount()](function.ocirowcount.html) є аліасом **ocinumrows()**Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.