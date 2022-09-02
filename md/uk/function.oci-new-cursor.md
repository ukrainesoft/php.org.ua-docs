---
navigation:
  - function.oci-new-connect.md: « ocinewconnect
  - function.oci-new-descriptor.md: ocinewdescriptor »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocinewcursor
---
# ocinewcursor

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinewcursor — Повертає ідентифікатор створеного курсору

### Опис

```methodsynopsis
oci_new_cursor(resource $connection): resource|false
```

Створює новий курсор для зазначеного з'єднання та повертає його ідентифікатор.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [ociconnect()](function.oci-connect.md) або [ocipconnect()](function.oci-pconnect.md)

### Значення, що повертаються

Повертає покажчик на новий вираз або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Прив'язка REF CURSOR у виклику процедур, що зберігаються Oracle**

```php
<?php

// Предварительная подготовка:
//   создайте или замените процедуру myproc(myrc out sys_refcursor) как
//   begin
//     open myrc for select first_name from employees;
//   end;

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$curs = oci_new_cursor($conn);
$stid = oci_parse($conn, "begin myproc(:cursbv); end;");
oci_bind_by_name($stid, ":cursbv", $curs, -1, OCI_B_CURSOR);
oci_execute($stid);

oci_execute($curs);  // Выполняет REF CURSOR как обычный идентификатор выражения
while (($row = oci_fetch_array($curs, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo $row['FIRST_NAME'] . "<br />\n";
}

oci_free_statement($stid);
oci_free_statement($curs);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocinewcursor()](function.ocinewcursor.md). У PHP 5.0.0 і вище [ocinewcursor()](function.ocinewcursor.md) є аліасом \*\*ocinewcursor()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
