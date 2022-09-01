---
navigation:
  - function.pg-lo-write.html: « pgлоwrite
  - function.pg-num-fields.html: пгnumfields »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пгmetadata
---
# пгmetadata

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгmetadata — Отримання метаданих таблиці

### Опис

```methodsynopsis
pg_meta_data(PgSql\Connection $connection, string $table_name, bool $extended = false): array|false
```

**пгmetadata()** повертає визначення таблиці `table_name` у вигляді масиву.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`table_name`

Назва таблиці.

`extended`

Прапор, що вказує, що потрібно повернути розширені мета-дані. За замовчуванням **`false`**

### Значення, що повертаються

Масив, що містить визначення таблиці або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Отримання метаданих таблиці**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с сервером");

  $meta = pg_meta_data($dbconn, 'authors');
  if (is_array($meta)) {
      echo '<pre>';
      var_dump($meta);
      echo '</pre>';
  }
?>
```

Результат виконання цього прикладу:

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

-   [пгconvert()](function.pg-convert.html) - Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
