---
navigation:
  - function.sqlsrv-rows-affected.md: « sqlsrv\_rows\_affected
  - function.sqlsrv-server-info.md: sqlsrv\_server\_info »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_send\_stream\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_send\_stream\_data

(No version information available, might only be in Git)

sqlsrv\_send\_stream\_data — Надсилання даних із потоків параметрів на сервер

### Опис

```methodsynopsis
sqlsrv_send_stream_data(resource $stmt): bool
```

Надсилати дані з потоків параметрів на сервер. Кожний дзвінок надсилає до 8 КБ даних.

### Список параметрів

`stmt`

Ресурс виразу, що повертається [sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_execute()](function.sqlsrv-execute.md)

### Значення, що повертаються

Повертає **`true`**, якщо є ще дані для відправки та **`false`**, якщо ні.

### Приклади

**Пример #1 Пример использования**sqlsrv\_send\_stream\_data()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ( ?) WHERE id = 100";

// Откройте данные параметров как поток и поместите их в массив $params.
$data = fopen( "data://text/plain,[ Lengthy content here. ]", "r");
$params = array( &$data);

// Подготовьте выражение. Используйте массив $options, чтобы
// отключить поведение по умолчанию, которое заключается в отправке всех данных
// потока во время выполнения запроса.
$options = array("SendStreamParamsAtExec"=>0);
$stmt = sqlsrv_prepare( $conn, $sql, $params, $options);

sqlsrv_execute( $stmt);

// Отправляйте до 8 КБ данных параметров на сервер
// при каждом вызове sqlsrv_send_stream_data.
$i = 1;
while( sqlsrv_send_stream_data( $stmt)) {
      $i++;
}
echo "$i вызовов было сделано.";
?>
```

### Дивіться також

-   [sqlsrv\_prepare()](function.sqlsrv-prepare.md) \- готує запит до виконання
-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
