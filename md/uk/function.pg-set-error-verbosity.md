Визначає обсяг тексту повідомлень, що повертаються функціями pglasterror та pgresulterror

-   [« pg\_set\_client\_encoding](function.pg-set-client-encoding.html)
    
-   [pg\_socket »](function.pg-socket.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Визначає обсяг тексту повідомлень, що повертаються функціями pglasterror та pgresulterror
    

# пгseterrorverbosity

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгseterrorverbosity — Визначає обсяг тексту повідомлень, що повертаються функціями [pg\_last\_error()](function.pg-last-error.html) і [pg\_result\_error()](function.pg-result-error.html)

### Опис

```methodsynopsis
pg_set_error_verbosity(PgSql\Connection $connection = ?, int $verbosity): int
```

Визначає обсяг тексту повідомлень, що повертаються функціями [pg\_last\_error()](function.pg-last-error.html) і [pg\_result\_error()](function.pg-result-error.html)

**пгseterrorverbosity()** встановлює режим, який відповідає за повноту повідомлень про помилки. В режимі **`PGSQL_ERRORS_TERSE`** повідомлення будуть містити лише важливість помилки, основний текст та місце виникнення; ця інформація зазвичай міститься в один рядок. У режимі за замовчуванням **`PGSQL_ERRORS_DEFAULT`** до повідомлень буде додано деталі помилки, підказка або поля контексту (це може зайняти кілька рядків). В режимі **`PGSQL_ERRORS_VERBOSE`** повідомлення будуть містити всі поля. Зміна режиму не торкнеться повідомлення існуючих ресурсів. Новий режим буде застосовуватися тільки до новостворених.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`verbosity`

Необхідний режим: **`PGSQL_ERRORS_TERSE`** **`PGSQL_ERRORS_DEFAULT`** або **`PGSQL_ERRORS_VERBOSE`**

### Значення, що повертаються

Попередній режим, що діяв до запуску функції: **`PGSQL_ERRORS_TERSE`** **`PGSQL_ERRORS_DEFAULT`** або **`PGSQL_ERRORS_VERBOSE`**

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгseterrorverbosity()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  pg_set_error_verbosity($dbconn, PGSQL_ERRORS_VERBOSE);
  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### Дивіться також

-   [pg\_last\_error()](function.pg-last-error.html) - Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [pg\_result\_error()](function.pg-result-error.html) - Повертає повідомлення про помилку, пов'язане із запитом результату