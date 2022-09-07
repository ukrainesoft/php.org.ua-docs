---
navigation:
  - function.pg-insert.md: « pginsert
  - function.pg-last-notice.md: пгlastnotice »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгlasterror
---
# пгlasterror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгlasterror — Отримує повідомлення про помилку, що відбулася на з'єднанні з базою даних.

### Опис

```methodsynopsis
pg_last_error(?PgSql\Connection $connection = null): string
```

**пгlasterror()** повертає повідомлення про останню помилку на заданому з'єднанні `connection`

Повідомлення про помилки можуть перезаписуватися під час внутрішніх викликів функцій PostgreSQL (libpq). Якщо всередині модуля PostgreSQL буде кілька помилок, повідомлення може виявитися неінформативним.

Для обробки помилок краще використовувати функції [пгresulterror()](function.pg-result-error.md) [пгresulterrorfield()](function.pg-result-error-field.md) [пгresultstatus()](function.pg-result-status.md) і [пгconnectionstatus()](function.pg-connection-status.md)

> **Зауваження**
> 
> Колишня назва функції: **пгerrormessage()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить повідомлення про останню помилку, що сталася на з'єднанні `connection`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгlasterror()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с сервером");

  // Неудачный запрос
  $res = pg_query($dbconn, "select * from doesnotexist");

  echo pg_last_error($dbconn);
?>
```

### Дивіться також

-   [пгresulterror()](function.pg-result-error.md) - Повертає повідомлення про помилку, пов'язане із запитом результату
-   [пгresulterrorfield()](function.pg-result-error-field.md) - Повертає конкретне поле зі звіту про помилки
