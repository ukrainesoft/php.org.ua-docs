---
navigation:
  - function.pg-escape-literal.md: « pg\_escape\_literal
  - function.pg-execute.md: pg\_execute »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_escape\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_escape\_string

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_escape\_string — Екранування спецсимволів у рядку запиту

### Опис

```methodsynopsis
pg_escape_string(PgSql\Connection $connection = ?, string $data): string
```

Функция**pg\_escape\_string()** екранує спецсимволи у рядку запиту для бази даних. Вона повертає екранований рядок у форматі PostgreSQL. Функція **pg\_escape\_string()** є найкращим способом екранування SQL параметрів для PostgreSQL, в той час як [addslashes()](function.addslashes.md) не має використовуватися з PostgreSQL. Якщо тип стовпця bytea, то має використовуватись функція [pg\_escape\_bytea()](function.pg-escape-bytea.md) замість pg\_escape\_string. Функция[pg\_escape\_identifier()](function.pg-escape-identifier.md) використовується для екранування ідентифікаторів (наприклад, імена таблиць або полів).

> **Зауваження** :
> 
> Функція підтримується PostgreSQL версії 7.2 та вище.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Вихідний рядок, що екранується.

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_escape\_string()\*\*\*\*

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Чтение текстового файла (содержащего апострофы и обратные слеши)
  $data = file_get_contents('letter.txt');

  // Экранирование спецсимволов в строке
  $escaped = pg_escape_string($data);

  // Вставка в таблицу базы данных
  pg_query("INSERT INTO correspondence (name, data) VALUES ('My letter', '{$escaped}')");
?>
```

### Дивіться також

-   [pg\_escape\_bytea()](function.pg-escape-bytea.md) \- Екранує спецсимволи у рядку для вставки у поле типу bytea
