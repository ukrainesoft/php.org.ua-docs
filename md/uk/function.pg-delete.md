---
navigation:
  - function.pg-dbname.md: « pg\_dbname
  - function.pg-end-copy.md: pg\_end\_copy »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_delete

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_delete — Видалення записів

### Опис

```methodsynopsis
pg_delete(    PgSql\Connection $connection,    string $table_name,    array $conditions,    int $flags = PGSQL_DML_EXEC): string|bool
```

**pg\_delete()** видаляє з таблиці записи, що відповідають ключам та значенням масиву `conditions`

Якщо `flags`указан,[pg\_convert()](function.pg-convert.md)применяется к`conditions` із зазначеними прапорами.

По умолчанию**pg\_delete()** передає необроблені значення. Значення мають бути екрановані або опція **`PGSQL_DML_ESCAPE`** має бути вказана . **`PGSQL_DML_ESCAPE`** укладає в лапки та екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зауважте, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. Ці параметри мають оброблятися відповідно до їх контекстів, тобто. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`table_name`

Ім'я таблиці, з якої видаляються записи.

`conditions`

Асоціативний масив, ключі якого відповідають іменам полів таблиці `table_name`, А значення відповідають значенням, що видаляються в цих колонках.

`flags`

Комбінація констант **`PGSQL_CONV_FORCE_NULL`** **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** \*\*`PGSQL_DML_ASYNC`** або **`PGSQL_DML_STRING`**Если константа**`PGSQL_DML_STRING`\*\*присутствует в аргументе`flags`, то функція поверне рядок, що містить запит. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функция[pg\_convert()](function.pg-convert.md) внутрішньо не викликається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає рядок, якщо у аргументі `flags`передана константа\*\*`PGSQL_DML_STRING`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_delete()\*\*\*\*

```php
<?php
  $db = pg_connect('dbname=foo');
  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/массив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $res = pg_delete($db, 'post_log', $_POST, PG_DML_ESCAPE);
  if ($res) {
      echo "Данные из POST удалены: $res\n";
  } else {
      echo "Пользователь отправил неверные входные данные\n";
  }
?>
```

### Дивіться також

-   [pg\_convert()](function.pg-convert.md) \- Перетворює значення асоціативного масиву на відповідний для SQL-запитів вид
