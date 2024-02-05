---
navigation:
  - function.pg-cancel-query.md: « pg\_cancel\_query
  - function.pg-close.md: pg\_close »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_client\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_client\_encoding

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

pg\_client\_encoding — отримання кодування клієнта.

### Опис

```methodsynopsis
pg_client_encoding(?PgSql\Connection $connection = null): string
```

PostgreSQL підтримує автоматичне перетворення наборів символів між сервером та клієнтом для деяких кодувань . **pg\_client\_encoding()** повертає клієнтське кодування у вигляді рядка, що є стандартним ідентифікатором кодування PostgreSQL.

> **Зауваження** :
> 
> Для роботи функції потрібно PostgreSQL версії 7.0 або вищою. У випадку, якщо libpg скомпільована без підтримки багатобайтових кодувань, **pg\_client\_encoding()** завжди повертає `SQL_ASCII`. Набір кодувань, що підтримуються, залежить від версії сервера БД і описаний в документації PostgreSQL.
> 
> Функція для дзвінка: **pg\_clientencoding()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Клієнтське кодування.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** pg\_client\_encoding()\*\*\*\*

```php
<?php
// Допустим, что $conn - соединение с базой данных, поддерживающей стандарт ISO-8859-1
$encoding = pg_client_encoding($conn);

echo "Кодировка клиента: ", $encoding, "\n";
?>
```

Результат виконання наведеного прикладу:

```
Кодировка клиента: ISO-8859-1
```

### Дивіться також

-   [pg\_set\_client\_encoding()](function.pg-set-client-encoding.md) \- Встановлює клієнтське кодування
