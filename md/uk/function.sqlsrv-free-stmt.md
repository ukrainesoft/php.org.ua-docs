---
navigation:
  - function.sqlsrv-field-metadata.md: « sqlsrvfieldmetadata
  - function.sqlsrv-get-config.md: sqlsrvgetconfig »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvfreestmt
---
# sqlsrvfreestmt

(No version information available, might only be in Git)

sqlsrvfreestmt — Звільняє всі ресурси для вказаного оператора

### Опис

```methodsynopsis
sqlsrv_free_stmt(resource $stmt): bool
```

Звільняє всі ресурси для вказаного оператора. Оператор не можна використовувати після того, як для нього була викликана функція **sqlsrvfreestmt()**. Якщо **sqlsrvfreestmt()** викликається у операторі, який змінює стан сервера, виконання оператора припиняється і оператор відкочується.

### Список параметрів

`stmt`

Оператор, ресурси якого потрібно звільнити. Зверніть увагу, що **`null`** - Припустиме значення параметра. Це дозволяє викликати функцію у скрипті кілька разів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvfreestmt()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

/*-------------------------------
     Здесь можно обработать результаты запроса.
-------------------------------*/

/* Освободите ресурсы для оператора */
sqlsrv_free_stmt( $stmt);

?>
```

### Примітки

Основна відмінність між **sqlsrvfreestmt()** і [sqlsrvcancel()](function.sqlsrv-cancel.md) полягає в тому, що ресурс оператора, скасований за допомогою [sqlsrvcancel()](function.sqlsrv-cancel.md), може бути повторно виконаний, якщо він був створений за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.md). Ресурс оператора, скасований за допомогою **sqlsrvfreestatement()**, не може бути повторно виконано.

### Дивіться також

-   [sqlsrvcancel()](function.sqlsrv-cancel.md) - скасовує оператор
