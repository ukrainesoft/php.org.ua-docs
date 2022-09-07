---
navigation:
  - function.pg-result-status.md: « pgresultstatus
  - function.pg-send-execute.md: пгsendexecute »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгselect
---
# пгselect

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгselect — Вибір запису з бази даних

### Опис

```methodsynopsis
pg_select(    PgSql\Connection $connection,    string $table_name,    array $conditions,    int $flags = PGSQL_DML_EXEC,    int $mode = PGSQL_ASSOC): array|string|false
```

**пгselect()** вибирає записи з бази даних, які відповідають умовам `field=>value`, заданим у масиві `conditions`

Якщо заданий аргумент `flags`, то до масиву `conditions` буде застосовано функцію [пгconvert()](function.pg-convert.md) з параметрами, заданими як аргумент.

За замовчуванням [пгinsert()](function.pg-insert.md) передає необроблені значення. Значення мають бути екрановані або опція PGSQLDMLESCAPE має бути вказана. PGSQLDMLESCAPE містить лапки і екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зверніть увагу, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

`table_name`

Назва таблиці, з якої вибираються дані.

`conditions`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`. Буде обрано лише ті рядки, значення полів яких збігатимуться зі значеннями масиву.

`flags`

Одна з констант **`PGSQL_CONV_FORCE_NULL`** **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** **`PGSQL_DML_ASYNC`** **`PGSQL_DML_STRING`** чи їх комбінація. Якщо `flags` містить **`PGSQL_DML_STRING`**, функція поверне рядок. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функція [пгconvert()](function.pg-convert.md) внутрішньо не викликається.

### Значення, що повертаються

Повертає рядок (string), якщо `flags` містить **`PGSQL_DML_STRING`**, інакше у разі успішного виконання функція повертає масив (array) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Доданий параметр `mode` |

### Приклади

**Приклад #1 Приклад використання **пгselect()****

```php
<?php
  $db = pg_connect('dbname=foo');
  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/Масив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $rec = pg_select($db, 'post_log', $_POST);
  if ($rec) {
      echo "Records selected\n";
      var_dump($rec);
  } else {
      echo "Должно быть переданы неверные данные\n";
  }
?>
```

### Дивіться також

-   [пгconvert()](function.pg-convert.md) - Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
