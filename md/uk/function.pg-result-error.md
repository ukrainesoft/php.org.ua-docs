---
navigation:
  - function.pg-result-error-field.md: « pg\_result\_error\_field
  - function.pg-result-seek.md: pg\_result\_seek »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_result\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_result\_error

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_result\_error — Повертає повідомлення про помилку, пов'язане із запитом результату

### Опис

```methodsynopsis
pg_result_error(PgSql\Result $result): string|false
```

**pg\_result\_error()** повертає повідомлення про будь-яку помилку, пов'язану з екземпляром `result`. Таким чином, можна отримати більш правильне повідомлення про помилку, ніж при використанні [pg\_last\_error()](function.pg-last-error.md)

Функция[pg\_result\_error\_field()](function.pg-result-error-field.md) може дати більш детальну інформацію про помилку, ніж **pg\_result\_error()**

Так как[pg\_query()](function.pg-query.md) повертає **`false`** у разі виникнення помилки запиту необхідно використовувати [pg\_send\_query()](function.pg-send-query.md) і [pg\_get\_result()](function.pg-get-result.md)для получения дескриптора результата.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Повертає рядок (string). Повертає порожній рядок, якщо помилки немає. Якщо є помилка, не пов'язана з параметром `result`, то повертається **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_result\_error()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### Дивіться також

-   [pg\_result\_error\_field()](function.pg-result-error-field.md) \- Повертає конкретне поле зі звіту про помилки
-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_send\_query()](function.pg-send-query.md) \- Надсилає асинхронний запит
-   [pg\_get\_result()](function.pg-get-result.md) \- Отримання результату асинхронного запиту
-   [pg\_last\_error()](function.pg-last-error.md) \- Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [pg\_last\_notice()](function.pg-last-notice.md) \- Повертає останнє повідомлення від сервера PostgreSQL
