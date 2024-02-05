---
navigation:
  - function.db2-rollback.md: « db2\_rollback
  - function.db2-set-option.md: db2\_set\_option »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_server\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_server\_info

(PECL ibm\_db2 >= 1.1.1)

db2\_server\_info — Повертає об'єкт із властивостями, що описують сервер бази даних DB2

### Опис

```methodsynopsis
db2_server_info(resource $connection): stdClass|false
```

Функція повертає об'єкт із властивостями лише для читання, які повертають інформацію про сервер баз даних IBM DB2, Cloudscape або Apache Derby. У наступній таблиці наведено властивості сервера бази даних:

**Властивості сервера бази даних**

| Название свойства | Тип возвращаемого значения | Опис |
| --- | --- | --- |
| DBMS\_NAME | string | Ім'я сервера бази даних, до якого ви підключені. Для серверів DB2 це комбінація `DB2`, за якою слідує операційна система, в якій працює сервер бази даних. |
| DBMS\_VER | string | Версія сервера бази даних у вигляді рядка "MM.mm.uuuu", де MM – це мажорна версія, mm – це мінорна версія, а uuuu – це патч-версія. Наприклад, "08.02.0001" означає мажорну версію 8, версію мінору 2 і патч-версію 1. |
| DB\_CODEPAGE | int | Кодова сторінка бази даних, до якої ви підключені. |
| DB\_NAME | string | Назва бази даних, до якої ви підключені. |
| DFT\_ISOLATION | string |  |
| Рівень ізоляції транзакції за промовчанням підтримується сервером: |  |  |

UR

Незавершене читання: зміни відразу видно всім паралельним транзакціям.

CS

Стабільність курсору: рядок, прочитаний однією транзакцією, може бути змінено та зафіксовано другою паралельною транзакцією.

RS

Стабільність читання: транзакція може додавати або видаляти рядки, що відповідають умові пошуку або транзакції, що очікує.

RR

Читання, що повторюються: дані, на які впливає очікувана транзакція, недоступні для інших транзакцій.

NC

Без фіксації: будь-які зміни видно наприкінці успішної операції. Явні комміти та відкати неприпустимі.

| | IDENTIFIER\_QUOTE\_CHAR | string | Символ, який використовується для позначення ідентифікатора. | | INST\_NAME | string | Примірник на сервері бази даних містить базу даних. | | ISOLATION\_OPTION | array | Масив параметрів ізоляції, які підтримує сервер бази даних. Параметри ізоляції описані як DFT\_ISOLATION. | | KEYWORDS | array | Масив ключових слів зарезервованих сервером бази даних. | | LIKE\_ESCAPE\_CLAUSE | bool |**`true`**, якщо сервер бази даних підтримує використання підстановочних знаків `%`и`_`. . **`false`**, якщо сервер бази даних не підтримує ці знаки підстановки. | | MAX\_COL\_NAME\_LEN | int | Максимальна довжина імені стовпця, яку підтримує сервер бази даних, виражена в байтах. | | MAX\_IDENTIFIER\_LEN | int | Максимальна довжина SQL-ідентифікатора, яку підтримує сервер бази даних, виражена в символах. | | MAX\_INDEX\_SIZE | int | Максимальний розмір стовпців, об'єднаних в індекс, який підтримує сервер бази даних, виражений в байтах. | | MAX\_PROC\_NAME\_LEN | int | Максимальна довжина імені процедури, яку підтримує сервер бази даних, виражена в байтах. | | MAX\_ROW\_SIZE | int | Максимальна довжина рядка в таблиці бази даних, яку підтримує сервер бази даних, виражена в байтах. | | MAX\_SCHEMA\_NAME\_LEN | int | Максимальна довжина імені схеми, яку підтримує сервер бази даних, виражена в байтах. | | MAX\_STATEMENT\_LEN | int | Максимальна довжина SQL-оператора, яку підтримує сервер бази даних, виражена в байтах. | | MAX\_TABLE\_NAME\_LEN | int | Максимальна довжина імені таблиці, яку підтримує сервер бази даних, виражена в байтах. | | NON\_NULLABLE\_COLUMNS | bool |**`true`**, якщо сервер бази даних підтримує стовпці, які можна визначити як NOT NULL, \*\*`false`\*\*Якщо сервер бази даних не підтримує стовпці, визначені як NOT NULL. | | PROCEDURES | bool | **`true`**, якщо сервер бази даних підтримує використання оператора CALL для виклику збережених процедур, \*\*`false`\*\*якщо сервер бази даних не підтримує оператор CALL. | | SPECIAL\_CHARS | string | Рядок, що містить усі символи, крім a-Z, 0-9 та підкреслення, які можна використовувати у імені ідентифікатора. | | SQL\_CONFORMANCE | string |

Рівень відповідності специфікації ANSI/ISO SQL-92, який пропонує сервер бази даних:

ENTRY

Відповідність початковому рівню SQL-92.

FIPS127

Перехідна відповідність FIPS-127-2.

FULL

Повна відповідність стандарту SQL-92.

INTERMEDIATE

Відповідність до середнього рівня SQL-92.

### Список параметрів

`connection`

Встановлює активне з'єднання клієнта DB2.

### Значення, що повертаються

Повертає об'єкт у разі успішного виклику функції або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** db2\_server\_info()\*\*\*\*

Щоб отримати інформацію про сервер, ви повинні передати дійсний ресурс підключення до бази даних **db2\_server\_info()**

```php
<?php

$conn = db2_connect('sample', 'db2inst1', 'ibmdb2');

$server = db2_server_info( $conn );

if ($server) {
    echo "DBMS_NAME: ";                 var_dump( $server->DBMS_NAME );
    echo "DBMS_VER: ";                  var_dump( $server->DBMS_VER );
    echo "DB_CODEPAGE: ";               var_dump( $server->DB_CODEPAGE );
    echo "DB_NAME: ";                   var_dump( $server->DB_NAME );
    echo "INST_NAME: ";                 var_dump( $server->INST_NAME );
    echo "SPECIAL_CHARS: ";             var_dump( $server->SPECIAL_CHARS );
    echo "KEYWORDS: ";                  var_dump( sizeof($server->KEYWORDS) );
    echo "DFT_ISOLATION: ";             var_dump( $server->DFT_ISOLATION );
    echo "ISOLATION_OPTION: ";
    $il = '';
    foreach( $server->ISOLATION_OPTION as $opt )
    {
       $il .= $opt." ";
    }
    var_dump( $il );
    echo "SQL_CONFORMANCE: ";           var_dump( $server->SQL_CONFORMANCE );
    echo "PROCEDURES: ";                var_dump( $server->PROCEDURES );
    echo "IDENTIFIER_QUOTE_CHAR: ";     var_dump( $server->IDENTIFIER_QUOTE_CHAR );
    echo "LIKE_ESCAPE_CLAUSE: ";        var_dump( $server->LIKE_ESCAPE_CLAUSE );
    echo "MAX_COL_NAME_LEN: ";          var_dump( $server->MAX_COL_NAME_LEN );
    echo "MAX_ROW_SIZE: ";              var_dump( $server->MAX_ROW_SIZE );
    echo "MAX_IDENTIFIER_LEN: ";        var_dump( $server->MAX_IDENTIFIER_LEN );
    echo "MAX_INDEX_SIZE: ";            var_dump( $server->MAX_INDEX_SIZE );
    echo "MAX_PROC_NAME_LEN: ";         var_dump( $server->MAX_PROC_NAME_LEN );
    echo "MAX_SCHEMA_NAME_LEN: ";       var_dump( $server->MAX_SCHEMA_NAME_LEN );
    echo "MAX_STATEMENT_LEN: ";         var_dump( $server->MAX_STATEMENT_LEN );
    echo "MAX_TABLE_NAME_LEN: ";        var_dump( $server->MAX_TABLE_NAME_LEN );
    echo "NON_NULLABLE_COLUMNS: ";      var_dump( $server->NON_NULLABLE_COLUMNS );

    db2_close($conn);
}
?>
```

Результат виконання наведеного прикладу:

```
DBMS_NAME: string(9) "DB2/LINUX"
DBMS_VER: string(10) "08.02.0000"
DB_CODEPAGE: int(1208)
DB_NAME: string(6) "SAMPLE"
INST_NAME: string(8) "db2inst1"
SPECIAL_CHARS: string(2) "@#"
KEYWORDS: int(179)
DFT_ISOLATION: string(2) "CS"
ISOLATION_OPTION: string(12) "UR CS RS RR "
SQL_CONFORMANCE: string(7) "FIPS127"
PROCEDURES: bool(true)
IDENTIFIER_QUOTE_CHAR: string(1) """
LIKE_ESCAPE_CLAUSE: bool(true)
MAX_COL_NAME_LEN: int(30)
MAX_ROW_SIZE: int(32677)
MAX_IDENTIFIER_LEN: int(18)
MAX_INDEX_SIZE: int(1024)
MAX_PROC_NAME_LEN: int(128)
MAX_SCHEMA_NAME_LEN: int(30)
MAX_STATEMENT_LEN: int(2097152)
MAX_TABLE_NAME_LEN: int(128)
NON_NULLABLE_COLUMNS: bool(true)
```

### Дивіться також

-   [db2\_client\_info()](function.db2-client-info.md) \- Повертає об'єкт із властивостями, що описують клієнта DB2
