---
navigation:
  - function.pg-last-error.md: « pglasterror
  - function.pg-last-oid.md: пгlastoid »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгlastnotice
---
# пгlastnotice

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

пгlastnotice — Повертає останнє повідомлення від сервера PostgreSQL

### Опис

```methodsynopsis
pg_last_notice(PgSql\Connection $connection, int $mode = PGSQL_NOTICE_LAST): array|string|bool
```

**пгlastnotice()** повертає останнє повідомлення згенероване сервером PostgreSQL на заданому з'єднанні `connection`. У деяких випадках сервер надсилає повідомлення, наприклад, при створенні в таблиці колонки типу `SERIAL`

Завдяки **пгlastnotice()** не потрібно робити зайвих запитів, щоб дізнатися надсилала ваша транзакція повідомлення чи ні.

Можна відключити відстеження сповіщень установкою до 1 параметра `pgsql.ignore_notice` у файлі php.ini.

Можна вимкнути журналування повідомлень установкою до значення 0 параметра `pgsql.log_notice` у файлі php.ini. Поки цей параметр встановлено на 0, повідомлення неможливо записати до журналу виконання.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

`mode`

Одна з констант **`PGSQL_NOTICE_LAST`** (Для повернення останнього повідомлення), **`PGSQL_NOTICE_ALL`** (для повернення всіх повідомлень) або **`PGSQL_NOTICE_CLEAR`** (Для очищення повідомлень).

### Значення, що повертаються

Рядок, що містить останнє повідомлення на заданому з'єднанні, якщо задана опція **`PGSQL_NOTICE_LAST`**, масив (array), якщо опція **`PGSQL_NOTICE_ALL`** та значення типу bool у разі опції **`PGSQL_NOTICE_CLEAR`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Доданий параметр `mode` |

### Приклади

**Приклад #1 Приклад використання **пгlastnotice()****

```php
<?php
  $pgsql_conn = pg_connect("dbname=mark host=localhost");

  $res = pg_query("CREATE TABLE test (id SERIAL)");

  $notice = pg_last_notice($pgsql_conn);

  echo $notice;
?>
```

Результат виконання цього прикладу:

```
CREATE TABLE will create implicit sequence "test_id_seq" for "serial" column "test.id"
```

### Дивіться також

-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгlasterror()](function.pg-last-error.md) - Отримує повідомлення про останню помилку на з'єднанні з базою даних.
