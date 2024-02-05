---
navigation:
  - function.pg-num-rows.md: « pg\_num\_rows
  - function.pg-parameter-status.md: pg\_parameter\_status »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_options
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_options

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_options — Отримання параметрів з'єднання з сервером баз даних

### Опис

```methodsynopsis
pg_options(?PgSql\Connection $connection = null): string
```

**pg\_options()** повертає рядок, що містить параметри з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить параметри з'єднання `connection`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_options()\*\*\*\*

```php
<?php
   $pgsql_conn = pg_connect("dbname=mark host=localhost");
   echo pg_options($pgsql_conn);
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
