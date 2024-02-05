---
navigation:
  - function.pg-set-error-context-visibility.md: « pg\_set\_error\_context\_visibility
  - function.pg-socket.md: pg\_socket »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_set\_error\_verbosity
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_set\_error\_verbosity

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_set\_error\_verbosity — Визначає обсяг тексту повідомлень, що повертаються функціями [pg\_last\_error()](function.pg-last-error.md) і [pg\_result\_error()](function.pg-result-error.md)

### Опис

```methodsynopsis
pg_set_error_verbosity(PgSql\Connection $connection = ?, int $verbosity): int
```

Визначає обсяг тексту повідомлень, що повертаються функціями [pg\_last\_error()](function.pg-last-error.md) і [pg\_result\_error()](function.pg-result-error.md)

**pg\_set\_error\_verbosity()**устанавливает режим, отвечающий за полноту сообщений об ошибках. В режиме**`PGSQL_ERRORS_TERSE`** повідомлення будуть містити лише важливість помилки, основний текст та місце виникнення; ця інформація зазвичай міститься в один рядок. У режимі за замовчуванням **`PGSQL_ERRORS_DEFAULT`** до повідомлень буде додано деталі помилки, підказка або поля контексту (це може зайняти кілька рядків). В режимі **`PGSQL_ERRORS_VERBOSE`** повідомлення будуть містити всі поля. Зміна режиму не торкнеться повідомлення існуючих ресурсів. Новий режим буде застосовуватися тільки до новостворених.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`verbosity`

Необхідний режим: **`PGSQL_ERRORS_TERSE`** **`PGSQL_ERRORS_DEFAULT`**или**`PGSQL_ERRORS_VERBOSE`**

### Значення, що повертаються

Попередній режим, що діяв до запуску функції: **`PGSQL_ERRORS_TERSE`** **`PGSQL_ERRORS_DEFAULT`**или**`PGSQL_ERRORS_VERBOSE`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_set\_error\_verbosity()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  pg_set_error_verbosity($dbconn, PGSQL_ERRORS_VERBOSE);
  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### Дивіться також

-   [pg\_last\_error()](function.pg-last-error.md) \- Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [pg\_result\_error()](function.pg-result-error.md) \- Повертає повідомлення про помилку, пов'язане із запитом результату
