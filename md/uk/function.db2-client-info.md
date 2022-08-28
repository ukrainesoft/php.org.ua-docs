Повертає об'єкт із властивостями, що описують клієнта DB2

-   [« db2\_bind\_param](function.db2-bind-param.html)
    
-   [db2\_close »](function.db2-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Повертає об'єкт із властивостями, що описують клієнта DB2
    

# db2clientinfo

(PECL ibmdb2> = 1.1.1)

db2clientinfo — Повертає об'єкт із властивостями, що описують клієнта DB2

### Опис

```methodsynopsis
db2_client_info(resource $connection): object
```

Ця функція повертає об'єкт з доступними лише для читання властивостями, що повертають інформацію про клієнта DB2. Ці властивості перелічені у таблиці:

**Властивості клієнта DB2**

| Имя свойства                                  | Возвращаемый тип | Описание                                                                                                                                                                              |
|-----------------------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| APPLCODEPAGE                                  | int              | Кодова сторінка програми.                                                                                                                                                             |
| CONNCODEPAGE                                  | int              | Кодова сторінка поточного з'єднання.                                                                                                                                                  |
| DATASOURCENAME                                | string           | Ім'я джерела даних (DSN), що використовується для створення поточного з'єднання.                                                                                                      |
| DRIVERNAME                                    | string           | Ім'я бібліотеки, що реалізує специфікацію DB2 Call Level Interface (CLI).                                                                                                             |
| DRIVERODBCVER                                 | string           | Версія ODBC, яку підтримує клієнт DB2. Повертає рядок "MM.mm", де MM – мажор, а mm – мінор. Клієнт DB2 завжди повертає "03.51".                                                       |
| DRIVERVER                                     | string           | Версія клієнта у вигляді рядка "MM.mm.uuuu", де MM – мажор, mm – мінор, а uuuu – рівень оновлення. Наприклад, "08.02.0001" означає мажорну версію 8, мінорну 2 та рівень оновлення 1. |
| ODBCSQLCONFORMANCE                            | string           |                                                                                                                                                                                       |
| Рівень підтримки клієнтом граматики ODBC SQL: |                  |                                                                                                                                                                                       |

MINIMUM

Мінімальна підтримка граматики ODBC SQL.

CORE

Базова підтримка граматики ODBC SQL.

EXTENDED

Розширена підтримка граматики ODBC SQL.

| | ODBCVER | string | Версія ODBC підтримує драйвер ODBC. Повертає рядок формату "MM.mm.rrrr", де MM – мажор, mm – мінор та rrrr – версія релізу. Клієнт DB2 завжди повертає "03.01.0000". |

### Список параметрів

`connection`

Встановлює активне з'єднання DB2.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **db2clientinfo()****

Для отримання інформації ви повинні передати коректний ресурс з'єднання **db2clientinfo()**

```php
<?php
$conn = db2_connect( 'SAMPLE', 'db2inst1', 'ibmdb2' );
$client = db2_client_info( $conn );

if ($client) {
    echo "DRIVER_NAME: ";           var_dump( $client->DRIVER_NAME );
    echo "DRIVER_VER: ";            var_dump( $client->DRIVER_VER );
    echo "DATA_SOURCE_NAME: ";      var_dump( $client->DATA_SOURCE_NAME );
    echo "DRIVER_ODBC_VER: ";       var_dump( $client->DRIVER_ODBC_VER );
    echo "ODBC_VER: ";              var_dump( $client->ODBC_VER );
    echo "ODBC_SQL_CONFORMANCE: ";  var_dump( $client->ODBC_SQL_CONFORMANCE );
    echo "APPL_CODEPAGE: ";         var_dump( $client->APPL_CODEPAGE );
    echo "CONN_CODEPAGE: ";         var_dump( $client->CONN_CODEPAGE );
}
else {
    echo "Error retrieving client information.
     Perhaps your database connection was invalid.";
}
db2_close($conn);

?>
```

Результат виконання цього прикладу:

```
DRIVER_NAME: string(8) "libdb2.a"
DRIVER_VER: string(10) "08.02.0001"
DATA_SOURCE_NAME: string(6) "SAMPLE"
DRIVER_ODBC_VER: string(5) "03.51"
ODBC_VER: string(10) "03.01.0000"
ODBC_SQL_CONFORMANCE: string(8) "EXTENDED"
APPL_CODEPAGE: int(819)
CONN_CODEPAGE: int(819)
```

### Дивіться також

-   [db2\_server\_info()](function.db2-server-info.html) - Повертає об'єкт із властивостями, що описують сервер бази даних DB2