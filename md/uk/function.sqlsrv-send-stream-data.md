---
navigation:
  - function.sqlsrv-rows-affected.html: « sqlsrvrowsaffected
  - function.sqlsrv-server-info.html: sqlsrvserverinfo »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvsendstreamdata
---
# sqlsrvsendstreamdata

(No version information available, might only be in Git)

sqlsrvsendstreamdata — Надсилання даних із потоків параметрів на сервер

### Опис

```methodsynopsis
sqlsrv_send_stream_data(resource $stmt): bool
```

Надсилати дані з потоків параметрів на сервер. Кожний дзвінок надсилає до 8 КБ даних.

### Список параметрів

`stmt`

Ресурс виразу, що повертається [sqlsrvquery()](function.sqlsrv-query.html) або [sqlsrvexecute()](function.sqlsrv-execute.md)

### Значення, що повертаються

Повертає **`true`**, якщо є ще дані для відправки та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **sqlsrvsendstreamdata()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ( ?) WHERE id = 100";

// Откройте данные параметров как поток и поместите их в Масив $params.
$data = fopen( "data://text/plain,[ Lengthy content here. ]", "r");
$params = array( &$data);

// Подготовьте выражение. Используйте Масив $options, чтобы
// отключить поведение по умолчанию, которое заключается в отправке всех данных
// потока во время выполнения запроса.
$options = array("SendStreamParamsAtExec"=>0);
$stmt = sqlsrv_prepare( $conn, $sql, $params, $options);

sqlsrv_execute( $stmt);

// Отправляйте до 8 КБ данных параметров на сервер
// при каждом вызове sqlsrv_send_stream_data.
$i = 1;
while( sqlsrv_send_stream_data( $stmt)) {
      $i++;
}
echo "$i вызовов было сделано.";
?>
```

### Дивіться також

-   [sqlsrvprepare()](function.sqlsrv-prepare.md) - готує запит до виконання
-   [sqlsrvquery()](function.sqlsrv-query.md) - готує та виконує запит
