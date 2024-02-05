---
navigation:
  - function.pg-result-status.md: « pg\_result\_status
  - function.pg-send-execute.md: pg\_send\_execute »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_select
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_select

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_select — Вибір запису з бази даних

### Опис

```methodsynopsis
pg_select(    PgSql\Connection $connection,    string $table_name,    array $conditions,    int $flags = PGSQL_DML_EXEC,    int $mode = PGSQL_ASSOC): array|string|false
```

**pg\_select()** вибирає записи з бази даних, які відповідають умовам `field=>value`, заданим у масиві `conditions`

Если задан параметр`flags`, то до масиву `conditions`будет применена функция[pg\_convert()](function.pg-convert.md) з параметрами, заданими як аргумент.

Если задан параметр`mode`, що повертається значення буде у вигляді масиву при **`PGSQL_NUM`**, ассоциативного массива при\*\*`PGSQL_ASSOC`\*\* (за замовчуванням) або і того, і іншого при **`PGSQL_BOTH`**

По умолчанию[pg\_insert()](function.pg-insert.md) передає необроблені значення. Значення мають бути екрановані або опція PGSQL\_DML\_ESCAPE має бути вказана. PGSQL\_DML\_ESCAPE містить лапки і екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зверніть увагу, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Назва таблиці, з якої вибираються дані.

`conditions`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`. Буде обрано лише ті рядки, значення полів яких збігатимуться зі значеннями масиву.

`flags`

Одна из констант\*\*`PGSQL_CONV_FORCE_NULL`\*\* **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** **`PGSQL_DML_ASYNC`** **`PGSQL_DML_STRING`** чи їх комбінація. Якщо `flags` містить **`PGSQL_DML_STRING`**, функція поверне рядок. Якщо встановлено **`PGSQL_DML_NO_CONV`**или**`PGSQL_DML_ESCAPE`**, то функция[pg\_convert()](function.pg-convert.md) внутрішньо не викликається.

`mode`

Одна из констант\*\*`PGSQL_ASSOC`\*\* **`PGSQL_NUM`**или**`PGSQL_BOTH`**Если установлено значение**`PGSQL_ASSOC`**, що повертається значення буде асоціативним масивом (array), при **`PGSQL_NUM`**возвращаемое значение будет массивом (array), а при**`PGSQL_BOTH`** значення, що повертається, буде і асоціативним і числовим індексованим масивом (array).

### Значення, що повертаються

Повертає рядок (string), якщо `flags` містить **`PGSQL_DML_STRING`**, інакше у разі успішного виконання функція повертає масив (array) або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.1.0 | Добавлен параметр`mode` |

### Приклади

**Пример #1 Пример использования**pg\_select()\*\*\*\*

```php
<?php
  $db = pg_connect('dbname=foo');
  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/массив. Для этих значений это не безопасно
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

-   [pg\_convert()](function.pg-convert.md) \- Перетворює значення асоціативного масиву на відповідний для SQL-запитів вид
