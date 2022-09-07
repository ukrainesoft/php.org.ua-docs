---
navigation:
  - function.pg-escape-identifier.md: « pgescapeidentifier
  - function.pg-escape-string.md: пгescapestring »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгescapeliteral
---
# пгescapeliteral

(PHP 5> = 5.4.4, PHP 7, PHP 8)

пгescapeliteral — Екранувати літерал під час вставлення в текстове поле

### Опис

```methodsynopsis
pg_escape_literal(PgSql\Connection $connection = ?, string $data): string
```

Функція **пгescapeliteral()** екранує літерал для запиту бази даних PostgreSQL Вона повертає екранований літерал у форматі PostgreSQL . **пгescapeliteral()** додає лапки до та після даних. Користувачі не повинні додавати лапки. Рекомендується використовувати цю функцію замість [пгescapestring()](function.pg-escape-string.md). Якщо тип стовпця – bytea, замість нього слід використовувати [пгescapebytea()](function.pg-escape-bytea.md). Для екранування ідентифікаторів (наприклад таблиці, імен полів) необхідно використовувати [пгescapeidentifier()](function.pg-escape-identifier.md)

> **Зауваження**
> 
> Ця функція має внутрішній код екранування і може використовуватися з PostgreSQL 8.4 або молодшої версії.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок (string), що містить текст для екранування.

### Значення, що повертаються

Рядок (string), що містить екранований текст.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгescapeliteral()****

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Чтение из текстового файла (содержащий апострофы и обратные косые черты)
  $data = file_get_contents('letter.txt');

  // Экранирование текстовых данных
  $escaped = pg_escape_literal($data);

  // Вставка их в базу данных. Обратите внимание, что вокруг {$escaped} нет кавычек
  pg_query("INSERT INTO correspondence (name, data) VALUES ('My letter', {$escaped})");
?>
```

### Дивіться також

-   [пгescapeidentifier()](function.pg-escape-identifier.md) - Екранує ідентифікатор для вставки у текстове поле
-   [пгescapebytea()](function.pg-escape-bytea.md) - Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [пгescapestring()](function.pg-escape-string.md) - Екранування спецсимволів у рядку запиту
