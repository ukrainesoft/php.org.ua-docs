---
navigation:
  - function.cubrid-field-flags.md: « cubridfieldflags
  - function.cubrid-field-name.md: cubridfieldname »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridfieldlen
---
# cubridfieldlen

(PECL CUBRID >= 8.3.0)

cubridfieldlen — Отримати максимальну довжину вказаного стовпця

### Опис

```methodsynopsis
cubrid_field_len(resource $result, int $field_offset): int
```

Функція повертає максимальну довжину зазначеного стовпця у разі успішного виконання або **`false`** у разі виникнення помилки.

### Список параметрів

`result`

`Result` отриманий з [cubridexecute()](function.cubrid-execute.md)

`field_offset`

Індекс поля у рядку результуючого набору . `field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Максимальна довжина у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfieldlen()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Наименование столбца", "Тип столбца", "Максимальная длина столбца");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len);
}

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Наименование столбца                   Тип столбца                   Максимальная длина столбца
host_year                      integer                        11
event_code                     integer                        11
athlete_code                   integer                        11
stadium_code                   integer                        11
nation_code                    char                           3
medal                          char                           1
game_date                      date                           10
```
