---
navigation:
  - function.pg-escape-identifier.md: « pg\_escape\_identifier
  - function.pg-escape-string.md: pg\_escape\_string »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_escape\_literal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_escape\_literal

(PHP 5 >= 5.4.4, PHP 7, PHP 8)

pg\_escape\_literal — Екранувати літерал під час вставлення в текстове поле

### Опис

```methodsynopsis
pg_escape_literal(PgSql\Connection $connection = ?, string $data): string
```

Функция**pg\_escape\_literal()** екранує літерал для запиту бази даних PostgreSQL Вона повертає екранований літерал у форматі PostgreSQL . **pg\_escape\_literal()** додає лапки до та після даних. Користувачі не повинні додавати лапки. Рекомендується використовувати цю функцію замість [pg\_escape\_string()](function.pg-escape-string.md). Якщо тип стовпця – bytea, замість нього слід використовувати [pg\_escape\_bytea()](function.pg-escape-bytea.md). Для екранування ідентифікаторів (наприклад, таблиці, імен полів) потрібно використовувати [pg\_escape\_identifier()](function.pg-escape-identifier.md)

> **Зауваження** :
> 
> Ця функція має внутрішній код екранування і може використовуватися з PostgreSQL 8.4 або молодшої версії.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок (string), що містить текст для екранування.

### Значення, що повертаються

Рядок (string), що містить екранований текст.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_escape\_literal()\*\*\*\*

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

-   [pg\_escape\_identifier()](function.pg-escape-identifier.md) \- Екранує ідентифікатор для вставки у текстове поле
-   [pg\_escape\_bytea()](function.pg-escape-bytea.md) \- Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.md) \- Екранування спецсимволів у рядку запиту
