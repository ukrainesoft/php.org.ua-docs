Отримати імена стовпців у результуючому наборі

-   [« cubrid\_col\_size](function.cubrid-col-size.html)
    
-   [cubrid\_column\_types »](function.cubrid-column-types.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримати імена стовпців у результуючому наборі
    

# cubridcolumnnames

(PECL CUBRID >= 8.3.0)

cubridcolumnnames — Отримати імена стовпців у результуючому наборі

### Опис

```methodsynopsis
cubrid_column_names(resource $req_identifier): array
```

Функція **cubridcolumnnames()** використовується для отримання імен стовпців у результуючому наборі, заданому в `req_identifier`

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Масив рядків, що містять імена стовпців, у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridcolumnnames()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Maxlen");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len);
}

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Column Names                   Column Types                   Column Maxlen
host_year                      integer                        11
event_code                     integer                        11
athlete_code                   integer                        11
stadium_code                   integer                        11
nation_code                    char                           3
medal                          char                           1
game_date                      date                           10
```

### Дивіться також

-   [cubrid\_prepare()](function.cubrid-prepare.html) - Підготовляє SQL-вираз до виконання
-   [cubrid\_execute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор
-   [cubrid\_column\_types()](function.cubrid-column-types.html) - Отримати типи стовпців у результуючому наборі