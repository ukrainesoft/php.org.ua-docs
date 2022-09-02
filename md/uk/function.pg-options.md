---
navigation:
  - function.pg-num-rows.md: « pgnumrows
  - function.pg-parameter-status.md: пгparameterstatus »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгoptions
---
# пгoptions

(PHP 4, PHP 5, PHP 7, PHP 8)

пгoptions — Отримання параметрів з'єднання з сервером баз даних

### Опис

```methodsynopsis
pg_options(?PgSql\Connection $connection = null): string
```

**пгoptions()** повертає рядок, що містить параметри з'єднання PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить параметри з'єднання `connection`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгoptions()****

```php
<?php
   $pgsql_conn = pg_connect("dbname=mark host=localhost");
   echo pg_options($pgsql_conn);
?>
```

### Дивіться також

-   [пгconnect()](function.pg-connect.md) - Відкриває з'єднання з базою даних PostgreSQL
