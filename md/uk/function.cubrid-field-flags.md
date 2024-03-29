---
navigation:
  - function.cubrid-fetch-row.md: « cubrid\_fetch\_row
  - function.cubrid-field-len.md: cubrid\_field\_len »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_field\_flags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_field\_flags

(PECL CUBRID >= 8.3.0)

cubrid\_field\_flags — Отримати рядок, який містить прапори стовпця за вказаним індексом

### Опис

```methodsynopsis
cubrid_field_flags(resource $result, int $field_offset): string
```

Функція повертає рядок, що містить прапори стовпця за вказаним індексом, розділені пробілом. Ви можете розбити рядок на окремі частини, використовуючи explode. Можливі значення прапорів: **`not_null`** **`primary_key`** **`unique_key`** **`foreign_key`** **`auto_increment`** **`shared`** **`reverse_index`** **`reverse_unique`** і **`timestamp`**

### Список параметрів

`result`

`Result` отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`field_offset`

Индекс поля в строке результирующего набора`field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Рядок з прапорами у разі успішного виконання.

**`false`** у разі некоректного значення field\_offset.

\-1, якщо SQL-запит був відмінним від SELECT типу.

### Приклади

**Приклад #1 Приклад використання** cubrid\_field\_flags()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$col_num = cubrid_num_cols($result);

printf("%-30s %s\n", "Имя поля", "Флаги поля");
for($i = 0; $i < $col_num; $i++) {
    printf("%-30s %s\n", cubrid_field_name($result, $i), cubrid_field_flags($result, $i));
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Наименование поля                Флаги поля
host_year                      not_null primary_key unique_key
event_code                     not_null primary_key unique_key foreign_key
athlete_code                   not_null primary_key unique_key foreign_key
stadium_code                   not_null
nation_code
medal
game_date
```
