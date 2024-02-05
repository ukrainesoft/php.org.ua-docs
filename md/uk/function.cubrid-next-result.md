---
navigation:
  - function.cubrid-move-cursor.md: « cubrid\_move\_cursor
  - function.cubrid-num-cols.md: cubrid\_num\_cols »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_next\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_next\_result

(PECL CUBRID >= 8.4.0)

cubrid\_next\_result — Отримує результат наступного запиту під час виконання кількох SQL-операторів.

### Опис

```methodsynopsis
cubrid_next_result(resource $result): bool
```

Функция**cubrid\_next\_result()** використовується для отримання результатів наступного запиту, якщо виконується кілька SQL-операторів та для [cubrid\_execute()](function.cubrid-execute.md)установлен флаг\*\*`CUBRID_EXEC_QUERY_ALL`\*\*

### Список параметрів

`result`

`result` із виклику функції [cubrid\_execute()](function.cubrid-execute.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_next\_result()\*\*\*\*

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");

$sql_stmt = "SELECT * FROM code; SELECT * FROM history WHERE host_year=2004 AND event_code=20281";
$res = cubrid_execute($conn, $sql_stmt, CUBRID_EXEC_QUERY_ALL);

get_result_info($res);
cubrid_next_result($res);
get_result_info($res);

function get_result_info($req)
{
    printf("\n------------ get_result_info --------------------\n");

    $row_num = cubrid_num_rows($req);
    $col_num = cubrid_num_cols($req);

    $column_name_list = cubrid_column_names($req);
    $column_type_list = cubrid_column_types($req);

    $column_last_name = cubrid_field_name($req, $col_num - 1);
    $column_last_table = cubrid_field_table($req, $col_num - 1);

    $column_last_type = cubrid_field_type($req, $col_num - 1);
    $column_last_len = cubrid_field_len($req, $col_num - 1);

    $column_1_flags = cubrid_field_flags($req, 1);

    printf("%-30s %d\n", "Количество строк:", $row_num);
    printf("%-30s %d\n", "Количество столбцов:", $col_num);
    printf("\n");

    printf("%-30s %-30s %-15s\n", "Названия столбцов", "Типы столбцов", "Длина столбцов");
    printf("------------------------------------------------------------------------------\n");

    $size = count($column_name_list);
    for($i = 0; $i < $size; $i++) {
        $column_len = cubrid_field_len($req, $i);
        printf("%-30s %-30s %-15s\n", $column_name_list[$i], $column_type_list[$i], $column_len);
    }
    printf("\n\n");

    printf("%-30s %s\n", "Название последнего столбца:", $column_last_name);
    printf("%-30s %s\n", "Таблица последнего столбца:", $column_last_table);
    printf("%-30s %s\n", "Тип последнего столбца:", $column_last_type);
    printf("%-30s %d\n", "Длина последнего столбца:", $column_last_len);
    printf("%-30s %s\n", "Флаги второго столбца:", $column_1_flags);

    printf("\n\n");
}
?>
```

Результат виконання наведеного прикладу:

```
------------ get_result_info --------------------
Row count:                     6
Column count:                  2

Названия столбцов                 Типы столбцов                   Длина столбцов
------------------------------------------------------------------------------
s_name                         char                           1
f_name                         varchar                        6


Название последнего столбца:          f_name
Таблица последнего столбца:           code
Тип последнего столбца:              varchar
Длина последнего столбца:            6
Флаги второго столбца:



------------ get_result_info --------------------
Количество строк:                    4
Количество столбцов:                  5

Названия столбцов                 Типы столбцов                   Длина столбцов
------------------------------------------------------------------------------
event_code                     integer                        11
athlete                        varchar                        40
host_year                      integer                        11
score                          varchar                        10
unit                           varchar                        5


Название последнего столбца:      unit
Таблица последнего столбца:       history
Тип последнего столбца:          varchar
Длина последнего столбца:        5
Флаги второго столбца:          not_null primary_key unique_key
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
