Отримати ім'я таблиці, якою належить вказаний стовпець

-   [« cubridfieldseek](function.cubrid-field-seek.html)
    
-   [cubridfieldtype »](function.cubrid-field-type.html)
    
-   [PHP Manual](index.md)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
    
-   Отримати ім'я таблиці, якою належить вказаний стовпець
    

# cubridfieldtable

(PECL CUBRID >= 8.3.0)

cubridfieldtable — Отримати ім'я таблиці, до якої належить зазначений стовпець

### Опис

```methodsynopsis
cubrid_field_table(resource $result, int $field_offset): string
```

Функція повертає ім'я таблиці, яка містить вказаний стовпець. Буває корисно під час роботи з великими запитами з JOIN.

### Список параметрів

`result`

`Result` отриманий з [cubridexecute()](function.cubrid-execute.html)

`field_offset`

Індекс поля у рядку результуючого набору . `field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ім'я таблиці у разі успішного виконання.

**`false`** якщо заданий некоректний fieldoffset.

1, якщо SQL-запит був відмінним від SELECT типу.

### Приклади

**Приклад #1 Приклад використання **cubridfieldtable()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM code");

$col_num = cubrid_num_cols($result);

printf("%-15s %-15s %s\n", "Таблица поля", "Наименовение поля", "Тип поля");
for($i = 0; $i < $col_num; $i++) {
    printf("%-15s %-15s %s\n",
        cubrid_field_table($result, $i), cubrid_field_name($result, $i), cubrid_field_type($result, $i));
}

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Таблица поля      Наименовение поля  Тип поля
code            s_name          char
code            f_name          varchar
```