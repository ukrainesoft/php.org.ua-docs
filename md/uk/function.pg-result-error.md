Повертає повідомлення про помилку, пов'язане із запитом результату

-   [« pg\_result\_error\_field](function.pg-result-error-field.html)
    
-   [pg\_result\_seek »](function.pg-result-seek.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає повідомлення про помилку, пов'язане із запитом результату
    

# пгresulterror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгresulterror — Повертає повідомлення про помилку, пов'язане із запитом результату

### Опис

```methodsynopsis
pg_result_error(PgSql\Result $result): string|false
```

**пгresulterror()** повертає повідомлення про будь-яку помилку, пов'язану з екземпляром `result`. Таким чином, можна отримати більш правильне повідомлення про помилку, ніж при використанні [pg\_last\_error()](function.pg-last-error.html)

Функція [pg\_result\_error\_field()](function.pg-result-error-field.html) може дати більш детальну інформацію про помилку, ніж **пгresulterror()**

Так як [pg\_query()](function.pg-query.html) повертає **`false`** у разі виникнення помилки запиту необхідно використовувати [pg\_send\_query()](function.pg-send-query.html) і [pg\_get\_result()](function.pg-get-result.html) для отримання результату дескриптора.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Повертає рядок (string). Повертає порожній рядок, якщо помилки немає. Якщо є помилка, не пов'язана з параметром `result`, то повертається **`false`**

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_result\_error\_field()](function.pg-result-error-field.html) - Повертає конкретне поле зі звіту про помилки
-   [pg\_query()](function.pg-query.html) - Виконує запит
-   [pg\_send\_query()](function.pg-send-query.html) - Надсилає асинхронний запит
-   [pg\_get\_result()](function.pg-get-result.html) - Отримання результату асинхронного запиту
-   [pg\_last\_error()](function.pg-last-error.html) - Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [pg\_last\_notice()](function.pg-last-notice.html) - Повертає останнє повідомлення від сервера PostgreSQL