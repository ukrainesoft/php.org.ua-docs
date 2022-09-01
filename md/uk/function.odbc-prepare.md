---
navigation:
  - function.odbc-pconnect.html: « odbcpconnect
  - function.odbc-primarykeys.html: odbcprimarykeys »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbcprepare
---
# odbcprepare

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcprepare — Підготовка запиту до виконання

### Опис

```methodsynopsis
odbc_prepare(resource $odbc, string $query): resource|false
```

Підготовка запиту до виконання. Ідентифікатор результату може бути використаний пізніше для виконання запиту за допомогою [odbcexecute()](function.odbc-execute.md)

Деякі бази даних (наприклад, IBM DB2, MS SQL Server та Oracle) підтримують процедури, що зберігаються, які приймають параметри типу IN, INOUT і OUT, як визначено в специфікації ODBC. Однак драйвер Unified ODBC в даний час підтримує лише параметри типу IN для збережених процедур.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.md)

`query`

Підготовлюваний запит у вигляді рядка.

### Значення, що повертаються

Повертає ідентифікатор результату ODBC, якщо команда SQL була успішно підготовлена. У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання [odbcexecute()](function.odbc-execute.md) і **odbcprepare()****

У даному коді значення $success дорівнюватиме **`true`**, тільки якщо всі три параметри myproc є параметрами IN:

```php
<?php
$a = 1;
$b = 2;
$c = 3;
$stmt    = odbc_prepare($conn, 'CALL myproc(?,?,?)');
$success = odbc_execute($stmt, array($a, $b, $c));
?>
```

Якщо потрібно викликати процедуру, що зберігається з використанням параметрів INOUT або OUT, рекомендується використовувати власний модуль для вашої бази даних (наприклад, [oci8](ref.oci8.md) для Oracle).

### Дивіться також

-   [odbcexecute()](function.odbc-execute.md) - Виконує запит
