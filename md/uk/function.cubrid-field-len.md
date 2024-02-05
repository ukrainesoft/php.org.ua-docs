---
navigation:
  - function.cubrid-field-flags.md: « cubrid\_field\_flags
  - function.cubrid-field-name.md: cubrid\_field\_name »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_field\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_field\_len

(PECL CUBRID >= 8.3.0)

cubrid\_field\_len — Отримати максимальну довжину вказаного стовпця

### Опис

```methodsynopsis
cubrid_field_len(resource $result, int $field_offset): int
```

Функція повертає максимальну довжину зазначеного стовпця у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Список параметрів

`result`

`Result` отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`field_offset`

Индекс поля в строке результирующего набора`field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Максимальна довжина у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_field\_len()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Наименование столбца", "Тип столбца", "Максимальная длина столбца");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len);
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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
