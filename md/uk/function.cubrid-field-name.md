---
navigation:
  - function.cubrid-field-len.md: « cubrid\_field\_len
  - function.cubrid-field-seek.md: cubrid\_field\_seek »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_field\_name

(PECL CUBRID >= 8.3.0)

cubrid\_field\_name — Отримати ім'я вказаного стовпця

### Опис

```methodsynopsis
cubrid_field_name(resource $result, int $field_offset): string
```

Функція повертає ім'я зазначеного стовпця у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Список параметрів

`result`

`Result`, отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`field_offset`

Индекс поля в строке результирующего набора`field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я стовпця у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_field\_name()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$col_num = cubrid_num_cols($result);

printf("%-30s %s\n", "Наименование поля", "Флаги поля");
for($i = 0; $i < $col_num; $i++) {
    printf("%-30s %s\n", cubrid_field_name($result, $i), cubrid_field_flags($result, $i));
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Наименование поля                 Флаги поля
host_year                      not_null primary_key unique_key
event_code                     not_null primary_key unique_key foreign_key
athlete_code                   not_null primary_key unique_key foreign_key
stadium_code                   not_null
nation_code
medal
game_date
```
