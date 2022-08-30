Отримати ім'я вказаного стовпця

-   [« cubridfieldlen](function.cubrid-field-len.html)
    
-   [cubridfieldseek »](function.cubrid-field-seek.html)
    
-   [PHP Manual](index.md)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
    
-   Отримати ім'я вказаного стовпця
    

# cubridfieldname

(PECL CUBRID >= 8.3.0)

cubridfieldname — Отримати ім'я вказаного стовпця

### Опис

```methodsynopsis
cubrid_field_name(resource $result, int $field_offset): string
```

Функція повертає ім'я зазначеного стовпця у разі успішного виконання або **`false`** у разі виникнення помилки.

### Список параметрів

`result`

`Result`, отриманий з [cubridexecute()](function.cubrid-execute.html)

`field_offset`

Індекс поля у рядку результуючого набору . `field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я стовпця у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfieldname()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$col_num = cubrid_num_cols($result);

printf("%-30s %s\n", "Наименование поля", "Флаги поля");
for($i = 0; $i < $col_num; $i++) {
    printf("%-30s %s\n", cubrid_field_name($result, $i), cubrid_field_flags($result, $i));
}

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

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