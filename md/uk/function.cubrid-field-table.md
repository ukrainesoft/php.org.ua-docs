---
navigation:
  - function.cubrid-field-seek.md: « cubrid\_field\_seek
  - function.cubrid-field-type.md: cubrid\_field\_type »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_field\_table
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_field\_table

(PECL CUBRID >= 8.3.0)

cubrid\_field\_table — Отримати ім'я таблиці, до якої належить зазначений стовпець

### Опис

```methodsynopsis
cubrid_field_table(resource $result, int $field_offset): string
```

Функція повертає ім'я таблиці, яка містить вказаний стовпець. Буває корисно під час роботи з великими запитами з JOIN.

### Список параметрів

`result`

`Result` отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`field_offset`

Индекс поля в строке результирующего набора`field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання.

**`false`** якщо заданий некоректний field\_offset.

\-1, якщо SQL-запит був відмінним від SELECT типу.

### Приклади

**Приклад #1 Приклад використання** cubrid\_field\_table()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM code");

$col_num = cubrid_num_cols($result);

printf("%-15s %-15s %s\n", "Таблица поля", "Наименовение поля", "Тип поля");
for($i = 0; $i < $col_num; $i++) {
    printf("%-15s %-15s %s\n",
        cubrid_field_table($result, $i), cubrid_field_name($result, $i), cubrid_field_type($result, $i));
}

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Таблица поля      Наименовение поля  Тип поля
code            s_name          char
code            f_name          varchar
```
