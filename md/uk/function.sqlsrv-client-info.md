---
navigation:
  - function.sqlsrv-cancel.md: « sqlsrv\_cancel
  - function.sqlsrv-close.md: sqlsrv\_close »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_client\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_client\_info

(No version information available, might only be in Git)

sqlsrv\_client\_info — Повертає інформацію про клієнта та зазначене підключення

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

**Масив, що повертається sqlsrv\_client\_info**

| Ключ | Опис |
| --- | --- |
| DriverDllName | SQLNCLI10.DLL |
| DriverODBCVer | Версія ODBC (xx.yy) |
| DriverVer | Версія SQL Server Native Client DLL (10.5.xxx) |
| ExtensionVer | Версія php\_sqlsrv.dll (2.0.xxx.x) |

### Приклади

**Пример #1 Пример использования**sqlsrv\_client\_info()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connOptions = array("UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connOptions );

if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

if( $client_info = sqlsrv_client_info( $conn)) {
    foreach( $client_info as $key => $value) {
        echo $key.": ".$value."<br />";
    }
} else {
    echo "Ошибка при получении информации о клиенте.<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_server\_info()](function.sqlsrv-server-info.md) \- Повертає інформацію про сервер
