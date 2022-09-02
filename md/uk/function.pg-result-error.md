---
navigation:
  - function.pg-result-error-field.md: « pgresulterrorfield
  - function.pg-result-seek.md: пгresultseek »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгresulterror
---
# пгresulterror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгresulterror — Повертає повідомлення про помилку, пов'язане із запитом результату

### Опис

```methodsynopsis
pg_result_error(PgSql\Result $result): string|false
```

**пгresulterror()** повертає повідомлення про будь-яку помилку, пов'язану з екземпляром `result`. Таким чином, можна отримати більш правильне повідомлення про помилку, ніж при використанні [пгlasterror()](function.pg-last-error.md)

Функція [пгresulterrorfield()](function.pg-result-error-field.md) може дати більш детальну інформацію про помилку, ніж **пгresulterror()**

Так як [пгquery()](function.pg-query.md) повертає **`false`** у разі виникнення помилки запиту необхідно використовувати [пгsendquery()](function.pg-send-query.md) і [пгgetresult()](function.pg-get-result.md) для отримання результату дескриптора.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

### Значення, що повертаються

Повертає рядок (string). Повертає порожній рядок, якщо помилки немає. Якщо є помилка, не пов'язана з параметром `result`, то повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгresulterror()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### Дивіться також

-   [пгresulterrorfield()](function.pg-result-error-field.md) - Повертає конкретне поле зі звіту про помилки
-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгsendquery()](function.pg-send-query.md) - Надсилає асинхронний запит
-   [пгgetresult()](function.pg-get-result.md) - Отримання результату асинхронного запиту
-   [пгlasterror()](function.pg-last-error.md) - Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [пгlastnotice()](function.pg-last-notice.md) - Повертає останнє повідомлення від сервера PostgreSQL
