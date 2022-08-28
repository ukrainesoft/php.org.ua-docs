Повертає інформацію про сервер

-   [« sqlsrv\_send\_stream\_data](function.sqlsrv-send-stream-data.html)
    
-   [Модули для работы с датой и временем »](refs.calendar.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Повертає інформацію про сервер
    

# sqlsrvserverinfo

(No version information available, might only be in Git)

sqlsrvserverinfo — Повертає інформацію про сервер

### Опис

```methodsynopsis
sqlsrv_server_info(resource $conn): array
```

Повертає інформацію про сервер.

### Список параметрів

`conn`

Ресурс підключення, який з'єднує клієнт та сервер.

### Значення, що повертаються

Повертає масив, описаний у таблиці:

**Повертається масив**

| CurrentDatabase | Подключённая база данных. |
| --- | --- |
| SQLServerVersion | Версія SQL Server. |
| SQLServerName | Ім'я сервера. |

### Приклади

**Приклад #1 Приклад використання **sqlsrvserverinfo()****

```php
<?php
$serverName = "serverName\sqlexpress";
$conn = sqlsrv_connect( $serverName);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$server_info = sqlsrv_server_info( $conn);
if( $server_info )
{
    foreach( $server_info as $key => $value) {
       echo $key.": ".$value."<br />";
    }
} else {
      die( print_r( sqlsrv_errors(), true));
}
?>
```

### Дивіться також

-   [sqlsrv\_client\_info()](function.sqlsrv-client-info.html) - Повертає інформацію про клієнта та зазначене підключення