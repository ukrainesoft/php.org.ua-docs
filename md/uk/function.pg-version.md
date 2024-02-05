---
navigation:
  - function.pg-update.md: « pg\_update
  - class.pgsql-connection.md: PgSql\\Connection »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_version

(PHP 5, PHP 7, PHP 8)

pg\_version — Повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера (якщо є)

### Опис

```methodsynopsis
pg_version(?PgSql\Connection $connection = null): array
```

**pg\_version()** повертає масив, що містить версії клієнта, протоколу клієнт-серверної взаємодії та сервера. Версії протоколу та сервера доступні, тільки якщо модуль PHP скомпільовано для PostgreSQL версії 7.4 або вище.

Для отримання детальної інформації про сервер використовуйте функцію [pg\_parameter\_status()](function.pg-parameter-status.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає масив із ключами `client` `protocol`и`server` та відповідними значеннями версій.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_version()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("host=localhost port=5432 dbname=mary")
     or die("Could not connect");

  $v = pg_version($dbconn);

  echo $v['client'];
?>
```

Результат виконання наведеного прикладу:

```
7.4
```

### Дивіться також

-   [pg\_parameter\_status()](function.pg-parameter-status.md) \- Перегляд поточних значень параметрів сервера
