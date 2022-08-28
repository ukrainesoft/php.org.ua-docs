Екранувати літерал при вставці у текстове поле

-   [« pg\_escape\_identifier](function.pg-escape-identifier.html)
    
-   [pg\_escape\_string »](function.pg-escape-string.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Екранувати літерал при вставці у текстове поле
    

# пгescapeliteral

(PHP 5> = 5.4.4, PHP 7, PHP 8)

пгescapeliteral — Екранувати літерал під час вставлення в текстове поле

### Опис

```methodsynopsis
pg_escape_literal(PgSql\Connection $connection = ?, string $data): string
```

Функція **пгescapeliteral()** екранує літерал для запиту бази даних PostgreSQL Вона повертає екранований літерал у форматі PostgreSQL . **пгescapeliteral()** додає лапки до та після даних. Користувачі не повинні додавати лапки. Рекомендується використовувати цю функцію замість [pg\_escape\_string()](function.pg-escape-string.html). Якщо тип стовпця – bytea, замість нього слід використовувати [pg\_escape\_bytea()](function.pg-escape-bytea.html). Для екранування ідентифікаторів (наприклад таблиці, імен полів) необхідно використовувати [pg\_escape\_identifier()](function.pg-escape-identifier.html)

> **Зауваження**
> 
> Ця функція має внутрішній код екранування і може використовуватися з PostgreSQL 8.4 або молодшої версії.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок (string), що містить текст для екранування.

### Значення, що повертаються

Рядок (string), що містить екранований текст.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгescapeliteral()****

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Чтение из текстового файла (содержащий апострофы и обратные косые черты)
  $data = file_get_contents('letter.txt');

  // Экранирование текстовых данных
  $escaped = pg_escape_literal($data);

  // Вставка их в базу данных. Обратите внимание, что вокруг {$escaped} нет кавычек
  pg_query("INSERT INTO correspondence (name, data) VALUES ('My letter', {$escaped})");
?>
```

### Дивіться також

-   [pg\_escape\_identifier()](function.pg-escape-identifier.html) - Екранує ідентифікатор для вставки у текстове поле
-   [pg\_escape\_bytea()](function.pg-escape-bytea.html) - Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.html) - Екранування спецсимволів у рядку запиту