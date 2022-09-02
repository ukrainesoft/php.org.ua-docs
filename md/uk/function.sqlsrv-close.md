---
navigation:
  - function.sqlsrv-client-info.md: « sqlsrvclientinfo
  - function.sqlsrv-commit.md: sqlsrvcommit »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvclose
---
# sqlsrvclose

(No version information available, might only be in Git)

sqlsrvclose — Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.

### Опис

```methodsynopsis
sqlsrv_close(resource $conn): bool
```

Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.

### Список параметрів

`conn`

З'єднання, яке потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvclose()****

```php
<?php
$serverName = "serverName\sqlexpres";
$connOptions = array("UID"=>"username", "PWD"=>"password", "Database"=>"dbname");
$conn = sqlsrv_connect( $serverName, $connOptions );
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

//-------------------------------------
// Выполнение операций с базой данных.
//-------------------------------------

// Закрытие соединения.
sqlsrv_close( $conn );
?>
```

### Дивіться також

-   [sqlsrvconnect()](function.sqlsrv-connect.md) - Відкриває з'єднання з базою даних Microsoft SQL Server
