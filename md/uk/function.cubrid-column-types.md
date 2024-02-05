---
navigation:
  - function.cubrid-column-names.md: « cubrid\_column\_names
  - function.cubrid-commit.md: cubrid\_commit »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_column\_types
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_column\_types

(PECL CUBRID >= 8.3.0)

cubrid\_column\_types — Отримати типи стовпців у результуючому наборі

### Опис

```methodsynopsis
cubrid_column_types(resource $req_identifier): array
```

Функция**cubrid\_column\_types()** використовується для отримання типів стовпців у результуючому наборі, заданому в `req_identifier`

### Список параметрів

`req_identifier`

Request identifier.

### Значення, що повертаються

Масив рядків, що містять типи стовпців, у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1**cubrid\_column\_types()**example**

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Maxlen");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len);
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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

-   [cubrid\_column\_names()](function.cubrid-column-names.md) \- Отримати імена стовпців у результуючому наборі
-   [cubrid\_prepare()](function.cubrid-prepare.md) \- Підготовляє SQL-вираз до виконання
-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
