---
navigation:
  - function.pg-untrace.md: « pg\_untrace
  - function.pg-version.md: pg\_version »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_update
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_update

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_update — Оновлення даних у таблиці

### Опис

```methodsynopsis
pg_update(    PgSql\Connection $connection,    string $table_name,    array $values,    array $conditions,    int $flags = PGSQL_DML_EXEC): string|bool
```

**pg\_update()** замінює записи у таблиці, що задовольняють умовам `conditions` даними `values`

Якщо `flags`указан,[pg\_convert()](function.pg-convert.md)применяется к`values` із зазначеними прапорами.

По умолчанию**pg\_update()** передає необроблені значення. Значення мають бути екрановані або опція **`PGSQL_DML_ESCAPE`** має бути вказана . **`PGSQL_DML_ESCAPE`** укладає в лапки та екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зверніть увагу, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці, де оновлюються записи.

`values`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`, а значення замінять дані у цих колонках.

`condition`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`. Буде оновлено лише рядки, значення полів яких збігатимуться зі значеннями масиву.

`flags`

Одна из констант\*\*`PGSQL_CONV_OPTS`\*\* **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** \*\*`PGSQL_DML_ASYNC`** або **`PGSQL_DML_STRING`\*\*або їх комбінація. Якщо `flags` містить **`PGSQL_DML_STRING`**, функція поверне рядок. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функция[pg\_convert()](function.pg-convert.md) внутрішньо не викликається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Функція поверне рядок (string), якщо константа **`PGSQL_DML_STRING`** міститься в `flags`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_update()\*\*\*\*

```php
<?php
  $db = pg_connect('dbname=foo');
  $data = array('field1'=>'AA', 'field2'=>'BB');

  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/массив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $res = pg_update($db, 'post_log', $_POST, $data);
  if ($res) {
      echo "Данные обновлены: $res\n";
  } else {
      echo "Должно быть переданы неверные данные\n";
  }
?>
```

### Дивіться також

-   [pg\_convert()](function.pg-convert.md) \- Перетворює значення асоціативного масиву на відповідний для SQL-запитів вид
