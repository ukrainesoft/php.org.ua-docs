---
navigation:
  - function.pg-dbname.html: « pgdbname
  - function.pg-end-copy.html: пгendcopy »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгdelete
---
# пгdelete

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгdelete — Видалення записів

### Опис

```methodsynopsis
pg_delete(    PgSql\Connection $connection,    string $table_name,    array $conditions,    int $flags = PGSQL_DML_EXEC): string|bool
```

**пгdelete()** видаляє з таблиці записи, що відповідають ключам та значенням масиву `conditions`

Якщо `flags` вказано, [пгconvert()](function.pg-convert.html) застосовується до `conditions` із зазначеними прапорами.

За замовчуванням **пгdelete()** передає необроблені значення. Значення повинні бути екрановані або опція **`PGSQL_DML_ESCAPE`** має бути вказана . **`PGSQL_DML_ESCAPE`** укладає в лапки та екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зауважте, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. Ці параметри мають оброблятися відповідно до їх контекстів, тобто. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`table_name`

Ім'я таблиці, з якої видаляються записи.

`conditions`

Асоціативний масив, ключі якого відповідають іменам полів таблиці `table_name`, А значення відповідають значенням, що видаляються в цих колонках.

`flags`

Комбінація констант **`PGSQL_CONV_FORCE_NULL`** **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** **`PGSQL_DML_ASYNC`** або **`PGSQL_DML_STRING`**. Якщо константа **`PGSQL_DML_STRING`** є в аргументі `flags`, то функція поверне рядок, що містить запит. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функція [пгconvert()](function.pg-convert.html) внутрішньо не викликається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає рядок, якщо у аргументі `flags` передана константа **`PGSQL_DML_STRING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгdelete()****

```php
<?php
  $db = pg_connect('dbname=foo');
  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/Масив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $res = pg_delete($db, 'post_log', $_POST, PG_DML_ESCAPE);
  if ($res) {
      echo "Данные из POST удалены: $res\n";
  } else {
      echo "Пользователь отправил неверные входные данные\n";
  }
?>
```

### Дивіться також

-   [пгconvert()](function.pg-convert.html) - Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах
