Повертає повідомлення про помилку, пов'язане із запитом результату

-   [« pgresulterrorfield](function.pg-result-error-field.html)
    
-   [пгresultseek »](function.pg-result-seek.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Повертає повідомлення про помилку, пов'язане із запитом результату
    

# пгresulterror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгresulterror — Повертає повідомлення про помилку, пов'язане із запитом результату

### Опис

```methodsynopsis
pg_result_error(PgSql\Result $result): string|false
```

**пгresulterror()** повертає повідомлення про будь-яку помилку, пов'язану з екземпляром `result`. Таким чином, можна отримати більш правильне повідомлення про помилку, ніж при використанні [пгlasterror()](function.pg-last-error.html)

Функція [пгresulterrorfield()](function.pg-result-error-field.html) може дати більш детальну інформацію про помилку, ніж **пгresulterror()**

Так як [пгquery()](function.pg-query.html) повертає **`false`** у разі виникнення помилки запиту необхідно використовувати [пгsendquery()](function.pg-send-query.html) і [пгgetresult()](function.pg-get-result.html) для отримання результату дескриптора.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Повертає рядок (string). Повертає порожній рядок, якщо помилки немає. Якщо є помилка, не пов'язана з параметром `result`, то повертається **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пгresulterrorfield()](function.pg-result-error-field.html) - Повертає конкретне поле зі звіту про помилки
-   [пгquery()](function.pg-query.html) - Виконує запит
-   [пгsendquery()](function.pg-send-query.html) - Надсилає асинхронний запит
-   [пгgetresult()](function.pg-get-result.html) - Отримання результату асинхронного запиту
-   [пгlasterror()](function.pg-last-error.html) - Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [пгlastnotice()](function.pg-last-notice.html) - Повертає останнє повідомлення від сервера PostgreSQL