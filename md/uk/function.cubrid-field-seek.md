---
navigation:
  - function.cubrid-field-name.md: « cubrid\_field\_name
  - function.cubrid-field-table.md: cubrid\_field\_table »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_field\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_field\_seek

(PECL CUBRID >= 8.3.0)

cubrid\_field\_seek — Перемістити внутрішній покажчик результуючого набору на вказаний стовпець

### Опис

```methodsynopsis
cubrid_field_seek(resource $result, int $field_offset = 0): bool
```

Функція переміщує внутрішній покажчик результуючого набору вказаний стовпець. Це усунення використовується функцією [cubrid\_fetch\_field()](function.cubrid-fetch-field.md), якщо не вказано параметр offset. Повертає **`true`**либо**`false`** залежно від успішності виконання.

### Список параметрів

`result`

`Result`, отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`field_offset`

Индекс поля в строке результирующего набора`field_offset` починається з 0. Якщо `field_offset` не заданий, то буде викликана помилка рівня **`E_WARNING`**

### Значення, що повертаються

**`true`** у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_field\_seek()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT event_code,athlete_code,nation_code,game_date FROM game WHERE host_year=1988 and event_code=20001;");

var_dump(cubrid_fetch_row($req));

cubrid_field_seek($req, 1);
$field = cubrid_fetch_field($req);

printf("\n--- Свойства поля ---\n");
printf("%-30s %s\n", "имя столбца:", $field->name);
printf("%-30s %s\n", "имя таблицы:", $field->table);
printf("%-30s \"%s\"\n", "значение столбца по умолчанию:", $field->def);
printf("%-30s %d\n", "максимальная длина столбца:", $field->max_length);
printf("%-30s %d\n", "не может быть NULL:", $field->not_null);
printf("%-30s %d\n", "является уникальным ключом:", $field->unique_key);
printf("%-30s %d\n", "является неуникальным ключом:", $field->multiple_key);
printf("%-30s %d\n", "содержит числовое значение:", $field->numeric);
printf("%-30s %s\n", "тип столбца:", $field->type);

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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
