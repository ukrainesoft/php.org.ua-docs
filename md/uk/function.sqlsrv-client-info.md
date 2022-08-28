Повертає інформацію про клієнта та зазначене підключення

-   [« sqlsrv\_cancel](function.sqlsrv-cancel.html)
    
-   [sqlsrv\_close »](function.sqlsrv-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Повертає інформацію про клієнта та зазначене підключення
    

# sqlsrvclientinfo

(No version information available, might only be in Git)

sqlsrvclientinfo — Повертає інформацію про клієнта та зазначене підключення

### Опис

```methodsynopsis
sqlsrv_client_info(resource $conn): array
```

Повертає інформацію про клієнта та зазначене підключення.

### Список параметрів

`conn`

З'єднання, про яке повертається інформація.

### Значення, що повертаються

Повертає асоціативний масив із ключами, описаними в таблиці нижче. В іншому випадку повертає **`false`**

**Масив, що повертається sqlsrvclientinfo**

| Ключ          | Описание                                       |
|---------------|------------------------------------------------|
| DriverDllName | SQLNCLI10.DLL                                  |
| DriverODBCVer | Версія ODBC (xx.yy)                            |
| DriverVer     | Версія SQL Server Native Client DLL (10.5.xxx) |
| ExtensionVer  | Версія phpsqlsrv.dll (2.0.xxx.x)               |

### Приклади

**Приклад #1 Приклад використання **sqlsrvclientinfo()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connOptions = array("UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connOptions );

if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

if( $client_info = sqlsrv_client_info( $conn)) {
    foreach( $client_info as $key => $value) {
        echo $key.": ".$value."<br />";
    }
} else {
    echo "Ошибка при получении информации о клиенте.<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_server\_info()](function.sqlsrv-server-info.html) - Повертає інформацію про сервер