Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах

-   [« pg\_consume\_input](function.pg-consume-input.html)
    
-   [pg\_copy\_from »](function.pg-copy-from.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
    

# пгconvert

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгconvert — Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах

### Опис

```methodsynopsis
pg_convert(    PgSql\Connection $connection,    string $table_name,    array $values,    int $flags = 0): array|false
```

**пгconvert()** перевіряє та перетворює значення з `values` у прийнятні для SQL-сервера. Необхідно, щоб існувала таблиця `table_name`, а кількість колонок у ній має бути не меншою, ніж значень у масиві `values`. Імена колонок у таблиці `table_name` повинні збігатися з ключами масиву `values`Типи даних значень масиву також повинні збігатися з типами даних відповідних колонок. У разі успішної конвертації функція повертає масив перетворених значень, інакше повертає **`false`**

> **Зауваження**
> 
> Булеві значення перетворюються на булев тип PostgreSQL. Строкові уявлення булевого значення також підтримуються . **`null`** перетворюється на PostgreSQL NULL.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

`table_name`

Ім'я таблиці бази даних.

`values`

Дані перетворення.

`flags`

Одна з констант **`PGSQL_CONV_IGNORE_DEFAULT`** **`PGSQL_CONV_FORCE_NULL`** або **`PGSQL_CONV_IGNORE_NOT_NULL`**або їх комбінація.

### Значення, що повертаються

Масив (array), що містить перетворені дані або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгconvert()****

```php
<?php
  $dbconn = pg_connect('dbname=foo');

  $tmp = array(
      'author' => 'Joe Thackery',
      'year' => 2005,
      'title' => 'My Life, by Joe Thackery'
  );

  $vals = pg_convert($dbconn, 'authors', $tmp);
?>
```

### Дивіться також

-   [pg\_meta\_data()](function.pg-meta-data.html) - Отримання метаданих таблиці
-   [pg\_insert()](function.pg-insert.html) - Заносить дані з масиву до таблиці бази даних
-   [pg\_select()](function.pg-select.html) - Вибирає записи із бази даних
-   [pg\_update()](function.pg-update.html) - Оновлення даних у таблиці
-   [pg\_delete()](function.pg-delete.html) - Видаляє записи