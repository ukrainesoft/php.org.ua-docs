---
navigation:
  - function.pg-insert.md: « pg\_insert
  - function.pg-last-notice.md: pg\_last\_notice »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_last\_error

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_last\_error — Отримує повідомлення про помилку, що відбулася, на з'єднанні з базою даних.

### Опис

```methodsynopsis
pg_last_error(?PgSql\Connection $connection = null): string
```

**pg\_last\_error()** повертає повідомлення про останню помилку на заданому з'єднанні `connection`

Повідомлення про помилки можуть перезаписуватися під час внутрішніх викликів функцій PostgreSQL (libpq). Якщо всередині модуля PostgreSQL буде кілька помилок, повідомлення може виявитися неінформативним.

Для обробки помилок краще використовувати функції [pg\_result\_error()](function.pg-result-error.md) [pg\_result\_error\_field()](function.pg-result-error-field.md) [pg\_result\_status()](function.pg-result-status.md) і [pg\_connection\_status()](function.pg-connection-status.md)

> **Зауваження** :
> 
> Прежнее название функции:**pg\_errormessage()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Строка, содержащая сообщение о последней ошибке, произошедшей на соединении`connection`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_last\_error()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с сервером");

  // Неудачный запрос
  $res = pg_query($dbconn, "select * from doesnotexist");

  echo pg_last_error($dbconn);
?>
```

### Дивіться також

-   [pg\_result\_error()](function.pg-result-error.md) \- Повертає повідомлення про помилку, пов'язане із запитом результату
-   [pg\_result\_error\_field()](function.pg-result-error-field.md) \- Повертає конкретне поле зі звіту про помилки
