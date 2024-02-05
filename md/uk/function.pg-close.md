---
navigation:
  - function.pg-client-encoding.md: « pg\_client\_encoding
  - function.pg-connect-poll.md: pg\_connect\_poll »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_close

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_close — Закриває з'єднання з базою даних PostgreSQL

### Опис

```methodsynopsis
pg_close(?PgSql\Connection $connection = null): true
```

**pg\_close()** закриває звичайне (непостійне) з'єднання з базою даних PostgreSQL, що відповідає екземпляру `connection`

> **Зауваження** :
> 
> Использование**pg\_close()**, зазвичай, необов'язково, оскільки непостійні з'єднання закриваються автоматично після завершення роботи скрипта.

Якщо зі з'єднанням працюють екземпляри [PgSql\\Lob](class.pgsql-lob.md), то перед закриттям з'єднання необхідно закрити всі екземпляри [PgSql\\Lob](class.pgsql-lob.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** pg\_close()\*\*\*\*

```php
<?php
$dbconn = pg_connect("host=localhost port=5432 dbname=mary")
   or die("Невозможно подключиться к БД");
echo "Успешно подключено к БД";
pg_close($dbconn);
?>
```

Результат виконання наведеного прикладу:

```
Успешно подключено к БД
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
