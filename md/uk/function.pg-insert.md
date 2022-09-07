---
navigation:
  - function.pg-host.md: « pghost
  - function.pg-last-error.md: пгlasterror »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгinsert
---
# пгinsert

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгinsert — Заносить дані з масиву до таблиці бази даних

### Опис

```methodsynopsis
pg_insert(    PgSql\Connection $connection,    string $table_name,    array $values,    int $flags = PGSQL_DML_EXEC): PgSql\Result|string|bool
```

**пгinsert()** вставляє записи з масиву `values` до таблиці `table_name`

Якщо `flags` вказано, [пгconvert()](function.pg-convert.md) застосовується до `values` із зазначеними прапорами.

За замовчуванням **пгinsert()** передає необроблені значення. Значення мають бути екрановані або опція **`PGSQL_DML_ESCAPE`** має бути вказана . **`PGSQL_DML_ESCAPE`** укладає в лапки та екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зверніть увагу, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці для вставлення даних. Кількість колонок у таблиці `table_name` має бути не менше, ніж елементів у масиві `values`

`values`

Асоціативний масив(array), у якому ключі є назвами колонок таблиці `table_name`а значення - записи, які необхідно вставити в ці колонки.

`flags`

Комбінація констант **`PGSQL_CONV_OPTS`** **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** **`PGSQL_DML_ASYNC`** і **`PGSQL_DML_STRING`**. Якщо серед інших передається **`PGSQL_DML_STRING`** у параметрі `flags`, функція поверне рядок запиту. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функція [пгconvert()](function.pg-convert.md) внутрішньо не викликається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.. Або повертає рядок(string), якщо **`PGSQL_DML_STRING`** включено до списку параметрів аргументу `flags`

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSqlResult](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгinsert()****

```php
<?php
  $dbconn = pg_connect('dbname=foo');
  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/Масив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $res = pg_insert($dbconn, 'post_log', $_POST);
  if ($res) {
      echo "Данные из POST успешно внесены в журнал\n";
  } else {
      echo "Пользователь прислал неверные данные\n";
  }
?>
```

### Дивіться також

-   [пгconvert()](function.pg-convert.md) - Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
