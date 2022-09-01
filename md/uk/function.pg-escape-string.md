---
navigation:
  - function.pg-escape-literal.html: « pgescapeliteral
  - function.pg-execute.html: пгexecute »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгescapestring
---
# пгescapestring

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгescapestring — Екранування спецсимволів у рядку запиту

### Опис

```methodsynopsis
pg_escape_string(PgSql\Connection $connection = ?, string $data): string
```

Функція **пгescapestring()** екранує спецсимволи у рядку запиту для бази даних. Вона повертає екранований рядок у форматі PostgreSQL. Функція **пгescapestring()** є найкращим способом екранування SQL параметрів для PostgreSQL, в той час як [addslashes()](function.addslashes.md) не має використовуватися з PostgreSQL. Якщо тип стовпця bytea, то має використовуватись функція [пгescapebytea()](function.pg-escape-bytea.html) замість pgescapestring. Функція [пгescapeidentifier()](function.pg-escape-identifier.md) використовується для екранування ідентифікаторів (наприклад, імена таблиць або полів).

> **Зауваження**
> 
> Функція підтримується PostgreSQL версії 7.2 та вище.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Вихідний рядок, що екранується.

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгescapestring()****

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Чтение текстового файла (содержащего апострофы и обратные слеши)
  $data = file_get_contents('letter.txt');

  // Экранирование спецсимволов в строке
  $escaped = pg_escape_string($data);

  // Вставка в таблицу базы данных
  pg_query("INSERT INTO correspondence (name, data) VALUES ('My letter', '{$escaped}')");
?>
```

### Дивіться також

-   [пгescapebytea()](function.pg-escape-bytea.md) - Екранує спецсимволи у рядку для вставки у поле типу bytea
