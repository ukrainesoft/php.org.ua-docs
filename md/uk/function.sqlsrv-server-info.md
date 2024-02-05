---
navigation:
  - function.sqlsrv-send-stream-data.md: « sqlsrv\_send\_stream\_data
  - refs.calendar.md: Модулі для роботи з датою та часом »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_server\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_server\_info

(No version information available, might only be in Git)

sqlsrv\_server\_info — Повертає інформацію про сервер

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

**Пример #1 Пример использования**sqlsrv\_server\_info()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$conn = sqlsrv_connect( $serverName);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$server_info = sqlsrv_server_info( $conn);
if( $server_info )
{
    foreach( $server_info as $key => $value) {
       echo $key.": ".$value."<br />";
    }
} else {
      die( print_r( sqlsrv_errors(), true));
}
?>
```

### Дивіться також

-   [sqlsrv\_client\_info()](function.sqlsrv-client-info.md) \- Повертає інформацію про клієнта та зазначене підключення
