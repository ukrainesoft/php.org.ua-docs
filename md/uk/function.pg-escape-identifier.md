---
navigation:
  - function.pg-escape-bytea.md: « pg\_escape\_bytea
  - function.pg-escape-literal.md: pg\_escape\_literal »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_escape\_identifier
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_escape\_identifier

(PHP 5 >= 5.4.4, PHP 7, PHP 8)

pg\_escape\_identifier — Екранує ідентифікатор для вставлення текстового поля

### Опис

```methodsynopsis
pg_escape_identifier(PgSql\Connection $connection = ?, string $data): string
```

**pg\_escape\_identifier()** екранує ідентифікатор (наприклад, таблицю, імена полів) виконання запиту до бази. Повертає екранований ідентифікатор рядка для сервера PostgreSQL . **pg\_escape\_identifier()** додає подвійні лапки до та після даних. Користувачі не повинні додавати подвійні лапки. Використання цієї функції рекомендується для налаштувань ідентифікаторів у запитах. Для SQL-літералів (тобто параметрів, крім bytea) необхідно використовувати [pg\_escape\_literal()](function.pg-escape-literal.md) або [pg\_escape\_string()](function.pg-escape-string.md). Для типу поля bytea потрібно використовувати [pg\_escape\_bytea()](function.pg-escape-bytea.md)

> **Зауваження** :
> 
> Ця функція має внутрішній код екранування та може бути використана з PostgreSQL 8.4 та нижче.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок (string), що містить текст, який має бути екранований.

### Значення, що повертаються

Рядок (string), що містить екрановані дані.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад виконання **pg\_escape\_identifier()****

```php
<?php
  // Установить соединение с базой данных
  $dbconn = pg_connect('dbname=foo');

  // Экранировать данные имени таблицы
  $escaped = pg_escape_identifier($table_name);

  // Выбрать строки из $table_name
  pg_query("SELECT * FROM {$escaped};");
?>
```

### Дивіться також

-   [pg\_escape\_literal()](function.pg-escape-literal.md) \- Екранувати літерал при вставці у текстове поле
-   [pg\_escape\_bytea()](function.pg-escape-bytea.md) \- Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.md) \- Екранування спецсимволів у рядку запиту
