---
navigation:
  - function.sqlsrv-client-info.md: « sqlsrv\_client\_info
  - function.sqlsrv-commit.md: sqlsrv\_commit »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_close

(No version information available, might only be in Git)

sqlsrv\_close — Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.

### Опис

```methodsynopsis
sqlsrv_close(resource $conn): bool
```

Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням.

### Список параметрів

`conn`

З'єднання, яке потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**sqlsrv\_close()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpres";
$connOptions = array("UID"=>"username", "PWD"=>"password", "Database"=>"dbname");
$conn = sqlsrv_connect( $serverName, $connOptions );
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

//-------------------------------------
// Выполнение операций с базой данных.
//-------------------------------------

// Закрытие соединения.
sqlsrv_close( $conn );
?>
```

### Дивіться також

-   [sqlsrv\_connect()](function.sqlsrv-connect.md) \- Відкриває з'єднання з базою даних Microsoft SQL Server
