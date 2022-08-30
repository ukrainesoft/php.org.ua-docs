Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням

-   [« sqlsrvclientinfo](function.sqlsrv-client-info.html)
    
-   [sqlsrvcommit »](function.sqlsrv-commit.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SQLSRV](ref.sqlsrv.html)
    
-   Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням
    

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

-   [sqlsrvconnect()](function.sqlsrv-connect.html) - Відкриває з'єднання з базою даних Microsoft SQL Server