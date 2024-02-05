---
navigation:
  - function.sqlsrv-connect.md: « sqlsrv\_connect
  - function.sqlsrv-execute.md: sqlsrv\_execute »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_errors
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_errors

(No version information available, might only be in Git)

sqlsrv\_errors — Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV

### Опис

```methodsynopsis
sqlsrv_errors(int $errorsOrWarnings = ?): mixed
```

Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV.

### Список параметрів

`errorsOrWarnings`

Визначає, чи повертаються відомості про помилки, попередження чи те й інше. Якщо параметр не вказано, повертаються як інформація про помилку, так і інформація про попередження. Підтримуються такі параметри: SQLSRV\_ERR\_ALL, SQLSRV\_ERR\_ERRORS, SQLSRV\_ERR\_WARNINGS.

### Значення, що повертаються

Якщо при останній операції sqlsrv виникли помилки та/або попередження, повертається масив масивів, що містять інформацію про помилки. Якщо при останній операції sqlsrv не було помилок та/або попереджень, повертається **`null`**. У наступній таблиці описана структура масивів, що повертаються:

**Масив, що повертається sqlsrv\_errors**

| Ключ | Опис |
| --- | --- |
| SQLSTATE | Для помилок, які виникають через драйвер ODBC, повертається SQLSTATE, що повертається ODBC. Для помилок, які виникають через драйвери Microsoft для PHP для SQL Server, SQLSTATE повертається IMSSP. Для попереджень, які виникають через драйвери Microsoft для PHP для SQL Server, SQLSTATE повертає значення 01SSP. |
| code | Для помилок, які виникають через SQL Server повертає власний код помилки SQL Server. Для помилок, що виникають через драйвер ODBC, повертається код помилки, який повертається ODBC. Для помилок, які виникають через драйвери Microsoft для PHP для SQL Server, повертається код помилки Microsoft Drivers для PHP для SQL Server. |
| message | Опис помилки. |

### Приклади

**Приклад #1 Приклад використання** functionname()\*\*\*\*

```php
<?php
$serverName = "serverName/sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

/* Настройка запроса для выборки недопустимого имени столбца. */
$sql = "SELECT BadColumnName FROM Table_1";

/* Выполнение запроса завершится ошибкой из-за неправильного имени столбца. */
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false ) {
    if( ($errors = sqlsrv_errors() ) != null) {
        foreach( $errors as $error ) {
            echo "SQLSTATE: ".$error[ 'SQLSTATE']."<br />";
            echo "Код: ".$error[ 'code']."<br />";
            echo "Сообщение: ".$error[ 'message']."<br />";
        }
    }
}
?>
```

### Примітки

За промовчанням попередження, що генеруються під час виклику будь-якої функції SQLSRV, обробляються як помилки. Це означає, що якщо під час виклику функції SQLSRV виникає попередження, функція повертає **`false`**. Проте попередження, що відповідають значенням SQLSTATE 01000, 01001, 01003 та 01S02, ніколи не розглядаються як помилки. Для отримання інформації про зміну цієї поведінки дивіться опис функції [sqlsrv\_configure()](function.sqlsrv-configure.md)и параметр WarningsReturnAsErrors.

### Дивіться також

-   [sqlsrv\_configure()](function.sqlsrv-configure.md) \- Змінює конфігурацію обробки помилок драйвера та ведення журналу
