Перемістити внутрішній покажчик результуючого набору на вказаний стовпець

-   [« cubridfieldname](function.cubrid-field-name.html)
    
-   [cubridfieldtable »](function.cubrid-field-table.html)
    
-   [PHP Manual](index.md)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
    
-   Перемістити внутрішній покажчик результуючого набору на вказаний стовпець
    

# cubridfieldseek

(PECL CUBRID >= 8.3.0)

cubridfieldseek — Перемістити внутрішній покажчик результуючого набору на вказаний стовпець

### Опис

```methodsynopsis
cubrid_field_seek(resource $result, int $field_offset = 0): bool
```

Функція переміщує внутрішній покажчик результуючого набору вказаний стовпець. Це усунення використовується функцією [cubridfetchfield()](function.cubrid-fetch-field.html), якщо не вказано параметр offset. Повертає **`true`** або **`false`** залежно від успішності виконання.

### Список параметрів

`result`

`Result`, отриманий з [cubridexecute()](function.cubrid-execute.html)

`field_offset`

Індекс поля у рядку результуючого набору . `field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

**`true`** у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfieldseek()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT event_code,athlete_code,nation_code,game_date FROM game WHERE host_year=1988 and event_code=20001;");

var_dump(cubrid_fetch_row($req));

cubrid_field_seek($req, 1);
$field = cubrid_fetch_field($req);

printf("\n--- Свойства поля ---\n");
printf("%-30s %s\n", "имя столбца:", $field->name);
printf("%-30s %s\n", "имя таблицы:", $field->table);
printf("%-30s \"%s\"\n", "значение столбца по умолчанию:", $field->def);
printf("%-30s %d\n", "максимальная длина столбца:", $field->max_length);
printf("%-30s %d\n", "не может быть NULL:", $field->not_null);
printf("%-30s %d\n", "является уникальным ключом:", $field->unique_key);
printf("%-30s %d\n", "является неуникальным ключом:", $field->multiple_key);
printf("%-30s %d\n", "содержит числовое значение:", $field->numeric);
printf("%-30s %s\n", "тип столбца:", $field->type);

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(4) {
  [0]=>
  string(5) "20001"
  [1]=>
  string(5) "16132"
  [2]=>
  string(3) "KOR"
  [3]=>
  string(9) "1988-09-30"
}

--- Свойства поля ---
имя столбца:                         athlete_code
имя таблицы:                         game
значение столбца по умолчанию:           ""
максимальная длина столбца:             0
не может быть NULL:                  1
является уникальным ключом:             1
является неуникальным ключом:           0
содержит числовое значение:             1
тип столбца:                          integer
```