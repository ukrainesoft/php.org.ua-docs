- [« pg_lo_write](function.pg-lo-write.md)
- [pg_num_fields »](function.pg-num-fields.md)

- [PHP Manual](index.md)
- [Функції PostgreSQL](ref.pgsql.md)
- Отримання метаданих таблиці

# pg_meta_data

(PHP 4 \>= 4.3.0, PHP 5, PHP 7, PHP 8)

pg_meta_data — Отримання метаданих таблиці

### Опис

**pg_meta_data**([PgSql\Connection](class.pgsql-connection.md)
`$connection`, string `$table_name`, bool `$extended` = **`false`**):
array\|false

**pg_meta_data()** повертає визначення таблиці `table_name` у вигляді
масиву.

### Список параметрів

`connection`
Примірник [PgSql\Connection](class.pgsql-connection.md).

`table_name`
Назва таблиці.

`extended`
Прапор, який вказує, що потрібно повернути розширені мета-дані. за
замовчуванням **`false`**.

### Значення, що повертаються

Масив, що містить визначення таблиці або **`false`** у разі
виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                                           |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.1.0  | Параметр connection тепер чекає на екземпляр [PgSql\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |

### Приклади

**Приклад #1 Отримання метаданих таблиці**

` <?php  $dbconn = pg_connect("dbname=publisher") or die("Не удалося з'єднатися з сервером"); $meta==pg_meta_data($dbconn, 'authors'); if (is_array($meta)) {      echo '<pre>'; var_dump($meta); echo '</pre>'; }?> `

Результат виконання цього прикладу:

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

### Дивіться також

- [pg_convert()](function.pg-convert.md) - Перетворює значення
асоціативного масиву прийнятні для використання в SQL-запитах
