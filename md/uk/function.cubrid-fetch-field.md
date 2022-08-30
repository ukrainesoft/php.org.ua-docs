Отримання інформації про стовпчик результуючого набору у вигляді об'єкта

-   [« cubridfetchassoc](function.cubrid-fetch-assoc.html)
    
-   [cubridfetchlengths »](function.cubrid-fetch-lengths.html)
    
-   [PHP Manual](index.html)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Отримання інформації про стовпчик результуючого набору у вигляді об'єкта
    

# cubridfetchfield

(PECL CUBRID >= 8.3.1)

cubridfetchfield — Отримання інформації про стовпчик результуючого набору у вигляді об'єкта

### Опис

```methodsynopsis
cubrid_fetch_field(resource $result, int $field_offset = 0): object
```

Функція повертає об'єкт, у властивостях якого міститься інформація про стовпчик. Властивості об'єкта:

`name`

ім'я стовпця

`table`

ім'я таблиці

`def`

значення стовпця за замовчуванням

`max_length`

максимальна довжина стовпця

`not_null`

1, якщо не може бути NULL

`primary_key`

1, якщо є первинним ключем

`unique_key`

1, якщо є унікальним ключем

`multiple_key`

1, якщо є неунікальним ключем

`numeric`

1, якщо містить числове значення

`blob`

1, якщо містить BLOB

`type`

тип стовпця

`unsigned`

1, якщо беззнаковий тип

`zerofill`

1, якщо доповнюється нулями

### Список параметрів

`result`

`Result`, отриманий з [cubridexecute()](function.cubrid-execute.html)

`field_offset`

Числовий індекс стовпця. Якщо не заданий, то буде вилучено наступний, не витягнутий цією функцією, стовпець . `field_offset` починається з нуля.

### Значення, що повертаються

Об'єкт із описаними вище властивостями у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfetchfield()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT event_code,athlete_code,nation_code,game_date FROM game WHERE host_year=1988 and event_code=20001;");

var_dump(cubrid_fetch_row($req));

cubrid_field_seek($req, 1);
$field = cubrid_fetch_field($req);

printf("\n--- Field Properties ---\n");
printf("%-30s %s\n", "имя столбца:", $field->name);
printf("%-30s %s\n", "имя таблицы:", $field->table);
printf("%-30s \"%s\"\n", "значение столбца по умолчанию:", $field->def);
printf("%-30s %d\n", "максимальная длина столбца:", $field->max_length);
printf("%-30s %d\n", "не может быть NULL:", $field->not_null);
printf("%-30s %d\n", "является первичным ключом:", $field->primary_key);
printf("%-30s %d\n", "является уникальным ключом:", $field->unique_key);
printf("%-30s %d\n", "является неуникальным ключом:", $field->multiple_key);
printf("%-30s %d\n", "содержит числовое значение:", $field->numeric);
printf("%-30s %d\n", "содержит BLOB:", $field->blob);
printf("%-30s %s\n", "тип столбца:", $field->type);
printf("%-30s %d\n", "беззнаковый тип:", $field->unsigned);
printf("%-30s %d\n", "дополняется нулями:", $field->zerofill);

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
  string(5) "16681"
  [2]=>
  string(3) "KOR"
  [3]=>
  string(9) "1988-9-30"
}

--- Field Properties ---
имя столбца:                         athlete_code
имя таблицы:                         game
значение столбца по умолчанию:          ""
максимальная длина столбца:             0
не может быть NULL:                  1
является первичным ключом:             1
является уникальным ключом:            1
является неуникальным ключом:           0
содержит числовое значение:             1
содержит BLOB:                       0
тип столбца:                         integer
беззнаковый тип:                      0
дополняется нулями:                    0
```