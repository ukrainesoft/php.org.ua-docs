Екранує ідентифікатор для вставки у текстове поле

-   [« pg\_escape\_bytea](function.pg-escape-bytea.html)
    
-   [pg\_escape\_literal »](function.pg-escape-literal.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Екранує ідентифікатор для вставки у текстове поле
    

# пгescapeidentifier

(PHP 5> = 5.4.4, PHP 7, PHP 8)

пгescapeidentifier — Екранує ідентифікатор для вставлення текстового поля

### Опис

```methodsynopsis
pg_escape_identifier(PgSql\Connection $connection = ?, string $data): string
```

**пгescapeidentifier()** екранує ідентифікатор (наприклад, таблицю, імена полів) виконання запиту до бази. Повертає екранований ідентифікатор рядка для сервера PostgreSQL . **пгescapeidentifier()** додає подвійні лапки до та після даних. Користувачі не повинні додавати подвійні лапки. Використання цієї функції рекомендується для налаштувань ідентифікаторів у запитах. Для SQL-літералів (тобто параметрів, крім bytea) необхідно використовувати [pg\_escape\_literal()](function.pg-escape-literal.html) або [pg\_escape\_string()](function.pg-escape-string.html). Для типу поля bytea потрібно використовувати [pg\_escape\_bytea()](function.pg-escape-bytea.html)

> **Зауваження**
> 
> Ця функція має внутрішній код екранування та може бути використана з PostgreSQL 8.4 та нижче.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок (string), що містить текст, який має бути екранований.

### Значення, що повертаються

Рядок (string), що містить екрановані дані.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад виконання **пгescapeidentifier()****

```php
<?php
  // Установить соединение с базой данных
  $dbconn = pg_connect('dbname=foo');

  // Экранировать данные имени таблицы
  $escaped = pg_escape_identifier($table_name);

  // Выбрать строки из $table_name
  pg_query("SELECT * FROM {$escaped};");
?>
```

### Дивіться також

-   [pg\_escape\_literal()](function.pg-escape-literal.html) - Екранувати літерал при вставці у текстове поле
-   [pg\_escape\_bytea()](function.pg-escape-bytea.html) - Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.html) - Екранування спецсимволів у рядку запиту