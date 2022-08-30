Отримати типи стовпців у результуючому наборі

-   [« cubridcolumnnames](function.cubrid-column-names.html)
    
-   [cubridcommit »](function.cubrid-commit.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Отримати типи стовпців у результуючому наборі
    

# cubridcolumntypes

(PECL CUBRID >= 8.3.0)

cubridcolumntypes — Отримати типи стовпців у результуючому наборі

### Опис

```methodsynopsis
cubrid_column_types(resource $req_identifier): array
```

Функція **cubridcolumntypes()** використовується для отримання типів стовпців у результуючому наборі, заданому в `req_identifier`

### Список параметрів

`req_identifier`

Request identifier.

### Значення, що повертаються

Масив рядків, що містять типи стовпців, у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **cubridcolumntypes()** example**

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

-   [cubridcolumnnames()](function.cubrid-column-names.html) - Отримати імена стовпців у результуючому наборі
-   [cubridprepare()](function.cubrid-prepare.html) - Підготовляє SQL-вираз до виконання
-   [cubridexecute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор