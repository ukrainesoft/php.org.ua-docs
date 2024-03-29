---
navigation:
  - function.db2-bind-param.md: « db2\_bind\_param
  - function.db2-close.md: db2\_close »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_client\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_client\_info

(PECL ibm\_db2 >= 1.1.1)

db2\_client\_info — Повертає об'єкт із властивостями, що описують клієнта DB2

### Опис

```methodsynopsis
db2_client_info(resource $connection): stdClass|false
```

Ця функція повертає об'єкт з доступними лише для читання властивостями, що повертають інформацію про клієнта DB2. Ці властивості перелічені у таблиці:

**Властивості клієнта DB2**

| Имя свойства | Возвращаемый тип | Опис |
| --- | --- | --- |
| APPL\_CODEPAGE | int | Кодова сторінка програми. |
| CONN\_CODEPAGE | int | Кодова сторінка поточного з'єднання. |
| DATA\_SOURCE\_NAME | string | Ім'я джерела даних (DSN), що використовується для створення поточного з'єднання. |
| DRIVER\_NAME | string | Ім'я бібліотеки, що реалізує специфікацію DB2 Call Level Interface (CLI). |
| DRIVER\_ODBC\_VER | string | Версія ODBC, яку підтримує клієнт DB2. Повертає рядок "MM.mm", де MM – мажор, а mm – мінор. Клієнт DB2 завжди повертає "03.51". |
| DRIVER\_VER | string | Версія клієнта у вигляді рядка "MM.mm.uuuu", де MM – мажор, mm – мінор, а uuuu – рівень оновлення. Наприклад, "08.02.0001" означає мажорну версію 8, мінорну 2 та рівень оновлення 1. |
| ODBC\_SQL\_CONFORMANCE | string |  |
| Рівень підтримки клієнтом граматики ODBC SQL: |  |  |

MINIMUM

Мінімальна підтримка граматики ODBC SQL.

CORE

Базова підтримка ODBC SQL граматики.

EXTENDED

Розширена підтримка граматики ODBC SQL.

| | ODBC\_VER | string | Версія ODBC підтримує драйвер ODBC. Повертає рядок формату "MM.mm.rrrr", де MM – мажор, mm – мінор та rrrr – версія релізу. Клієнт DB2 завжди повертає "03.01.0000". |

### Список параметрів

`connection`

Встановлює активне з'єднання DB2.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** db2\_client\_info()\*\*\*\*

Для отримання інформації ви повинні передати коректний ресурс з'єднання **db2\_client\_info()**

```php
<?php
$conn = db2_connect( 'SAMPLE', 'db2inst1', 'ibmdb2' );
$client = db2_client_info( $conn );

if ($client) {
    echo "DRIVER_NAME: ";           var_dump( $client->DRIVER_NAME );
    echo "DRIVER_VER: ";            var_dump( $client->DRIVER_VER );
    echo "DATA_SOURCE_NAME: ";      var_dump( $client->DATA_SOURCE_NAME );
    echo "DRIVER_ODBC_VER: ";       var_dump( $client->DRIVER_ODBC_VER );
    echo "ODBC_VER: ";              var_dump( $client->ODBC_VER );
    echo "ODBC_SQL_CONFORMANCE: ";  var_dump( $client->ODBC_SQL_CONFORMANCE );
    echo "APPL_CODEPAGE: ";         var_dump( $client->APPL_CODEPAGE );
    echo "CONN_CODEPAGE: ";         var_dump( $client->CONN_CODEPAGE );
}
else {
    echo "Error retrieving client information.
     Perhaps your database connection was invalid.";
}
db2_close($conn);

?>
```

Результат виконання наведеного прикладу:

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

-   [db2\_server\_info()](function.db2-server-info.md) \- Повертає об'єкт із властивостями, що описують сервер бази даних DB2
