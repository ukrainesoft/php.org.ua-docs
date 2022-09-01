---
navigation:
  - function.pg-update.html: « pgupdate
  - class.pgsql-connection.html: PgSqlConnection »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пгversion
---
# пгversion

(PHP 5, PHP 7, PHP 8)

пгversion — Повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера (якщо є)

### Опис

```methodsynopsis
pg_version(?PgSql\Connection $connection = null): array
```

**пгversion()** повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера. Версії протоколу та сервера доступні, тільки якщо модуль PHP скомпільовано для PostgreSQL версії 7.4 або вище.

Для отримання детальної інформації про сервер використовуйте функцію [пгparameterstatus()](function.pg-parameter-status.html)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає масив із ключами `client` `protocol` і `server` та відповідними значеннями версій.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгversion()****

```php
<?php
  $dbconn = pg_connect("host=localhost port=5432 dbname=mary")
     or die("Could not connect");

  $v = pg_version($dbconn);

  echo $v['client'];
?>
```

Результат виконання цього прикладу:

```
7.4
```

### Дивіться також

-   [пгparameterstatus()](function.pg-parameter-status.html) - Перегляд поточних значень параметрів сервера
