---
navigation:
  - function.pg-lo-write.md: « pg\_lo\_write
  - function.pg-num-fields.md: pg\_num\_fields »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_meta\_data
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_meta\_data

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_meta\_data — Отримання метаданих таблиці

### Опис

```methodsynopsis
pg_meta_data(PgSql\Connection $connection, string $table_name, bool $extended = false): array|false
```

**pg\_meta\_data()** повертає визначення таблиці `table_name` у вигляді масиву.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Назва таблиці.

`extended`

Прапор, що вказує, що потрібно повернути розширені мета-дані. За замовчуванням **`false`**

### Значення, що повертаються

Масив, що містить визначення таблиці або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання метаданих таблиці**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с сервером");

  $meta = pg_meta_data($dbconn, 'authors');
  if (is_array($meta)) {
      echo '<pre>';
      var_dump($meta);
      echo '</pre>';
  }
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
["author"]=>
array(5) {
  ["num"]=>
  int(1)
  ["type"]=>
  string(7) "varchar"
  ["len"]=>
  int(-1)
  ["not null"]=>
  bool(false)
  ["has default"]=>
  bool(false)
}
["year"]=>
array(5) {
  ["num"]=>
  int(2)
  ["type"]=>
  string(4) "int2"
  ["len"]=>
  int(2)
  ["not null"]=>
  bool(false)
  ["has default"]=>
  bool(false)
}
["title"]=>
array(5) {
  ["num"]=>
  int(3)
  ["type"]=>
  string(7) "varchar"
  ["len"]=>
  int(-1)
  ["not null"]=>
  bool(false)
  ["has default"]=>
  bool(false)
}
}
```

### Дивіться також

-   [pg\_convert()](function.pg-convert.md) \- Перетворює значення асоціативного масиву на відповідний для SQL-запитів вид
