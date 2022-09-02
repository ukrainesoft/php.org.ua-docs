---
navigation:
  - function.pg-client-encoding.md: « pgclientencoding
  - function.pg-connect-poll.md: пгconnectpoll »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгclose
---
# пгclose

(PHP 4, PHP 5, PHP 7, PHP 8)

пгclose — Закриває з'єднання з базою даних PostgreSQL

### Опис

```methodsynopsis
pg_close(?PgSql\Connection $connection = null): bool
```

**пгclose()** закриває звичайне (непостійне) з'єднання з базою даних PostgreSQL, що відповідає екземпляру `connection`

> **Зауваження**
> 
> Використання **пгclose()**, зазвичай, необов'язково, оскільки непостійні з'єднання закриваються автоматично після завершення роботи скрипта.

Якщо зі з'єднанням працюють екземпляри [PgSqlLob](class.pgsql-lob.md), то перед закриттям з'єднання необхідно закрити всі екземпляри [PgSqlLob](class.pgsql-lob.md)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгclose()****

```php
<?php
$dbconn = pg_connect("host=localhost port=5432 dbname=mary")
   or die("Невозможно подключиться к БД");
echo "Успешно подключено к БД";
pg_close($dbconn);
?>
```

Результат виконання цього прикладу:

```
Успешно подключено к БД
```

### Дивіться також

-   [пгconnect()](function.pg-connect.md) - Відкриває з'єднання з базою даних PostgreSQL
