---
navigation:
  - function.pg-last-error.md: « pg\_last\_error
  - function.pg-last-oid.md: pg\_last\_oid »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_last\_notice
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_last\_notice

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

pg\_last\_notice — Повертає останнє повідомлення від сервера PostgreSQL

### Опис

```methodsynopsis
pg_last_notice(PgSql\Connection $connection, int $mode = PGSQL_NOTICE_LAST): array|string|bool
```

\*\*pg\_last\_notice()\*\*возвращает последнее уведомление, сгенерированное сервером PostgreSQL на заданном соединении`connection`. У деяких випадках сервер надсилає повідомлення, наприклад, при створенні в таблиці колонки типу `SERIAL`

Благодаря**pg\_last\_notice()** не потрібно робити зайвих запитів, щоб дізнатися надсилала ваша транзакція повідомлення чи ні.

Можно отключить отслеживание уведомлений установкой в значение 1 параметра`pgsql.ignore_notice`в файле php.ini.

Можна вимкнути журналування повідомлень налаштуванням у значення 0 параметра `pgsql.log_notice` у файлі php.ini. Поки цей параметр встановлено на 0, повідомлення неможливо записати до журналу виконання.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`mode`

Одна из констант\*\*`PGSQL_NOTICE_LAST`**(для возврата последнего уведомления),**`PGSQL_NOTICE_ALL`**(для возврата всех уведомлений) или**`PGSQL_NOTICE_CLEAR`\*\*(для очистки уведомлений).

### Значення, що повертаються

Строка, содержащая последнее уведомление на заданном соединении, если задана опция\*\*`PGSQL_NOTICE_LAST`\*\*, масив (array), якщо опція **`PGSQL_NOTICE_ALL`**и значение типа bool в случае опции**`PGSQL_NOTICE_CLEAR`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.1.0 | Добавлен параметр`mode` |

### Приклади

**Пример #1 Пример использования**pg\_last\_notice()\*\*\*\*

```php
<?php
  $pgsql_conn = pg_connect("dbname=mark host=localhost");

  $res = pg_query("CREATE TABLE test (id SERIAL)");

  $notice = pg_last_notice($pgsql_conn);

  echo $notice;
?>
```

Результат виконання наведеного прикладу:

```
CREATE TABLE will create implicit sequence "test_id_seq" for "serial" column "test.id"
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_last\_error()](function.pg-last-error.md) \- Отримує повідомлення про останню помилку на з'єднанні з базою даних.
