---
navigation:
  - function.pg-consume-input.md: « pg\_consume\_input
  - function.pg-copy-from.md: pg\_copy\_from »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_convert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_convert

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_convert — Перетворює значення асоціативного масиву на відповідний для SQL-запитів вид

### Опис

```methodsynopsis
pg_convert(    PgSql\Connection $connection,    string $table_name,    array $values,    int $flags = 0): array|false
```

Функция**pg\_convert()** перевіряє та перетворює значення параметра `values` у прийнятні для SQL-сервера. Необхідно, щоб існувала таблиця `table_name`, а кількість колонок у ній має бути не меншою, ніж значень у масиві `values`Имена колонок в таблице`table_name` повинні збігатися з ключами масиву `values`Типи даних значень масиву також повинні збігатися з типами даних відповідних колонок. У разі успішної конвертації функція повертає масив перетворених значень, інакше повертає **`false`**

> **Зауваження** :
> 
> Логічні значення перетворюються на логічний тип PostgreSQL. Строкові уявлення логічного значення також підтримуються. Значення **`null`** перетворюється на PostgreSQL NULL.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці бази даних.

`values`

Дані перетворення.

`flags`

Одна из констант\*\*`PGSQL_CONV_IGNORE_DEFAULT`\*\* \*\*`PGSQL_CONV_FORCE_NULL`** або **`PGSQL_CONV_IGNORE_NOT_NULL`\*\*або їх комбінація.

### Значення, що повертаються

Масив (array), що містить перетворені дані або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад использования функции**pg\_convert()\*\*\*\*

```php
<?php
  $dbconn = pg_connect('dbname=foo');

  $tmp = array(
      'author' => 'Joe Thackery',
      'year' => 2005,
      'title' => 'My Life, by Joe Thackery'
  );

  $vals = pg_convert($dbconn, 'authors', $tmp);
?>
```

### Дивіться також

-   [pg\_meta\_data()](function.pg-meta-data.md) \- Отримання метаданих таблиці
-   [pg\_insert()](function.pg-insert.md) \- Заносить дані з масиву до таблиці бази даних
-   [pg\_select()](function.pg-select.md) \- Вибирає записи із бази даних
-   [pg\_update()](function.pg-update.md) \- Оновлення даних у таблиці
-   [pg\_delete()](function.pg-delete.md) \- Видаляє записи
