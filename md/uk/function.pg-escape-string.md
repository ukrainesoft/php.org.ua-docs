Екранування спецсимволів у рядку запиту

-   [« pg\_escape\_literal](function.pg-escape-literal.html)
    
-   [pg\_execute »](function.pg-execute.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Екранування спецсимволів у рядку запиту
    

# пгescapestring

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгescapestring — Екранування спецсимволів у рядку запиту

### Опис

```methodsynopsis
pg_escape_string(PgSql\Connection $connection = ?, string $data): string
```

Функція **пгescapestring()** екранує спецсимволи у рядку запиту для бази даних. Вона повертає екранований рядок у форматі PostgreSQL. Функція **пгescapestring()** є найкращим способом екранування SQL параметрів для PostgreSQL, в той час як [addslashes()](function.addslashes.html) не має використовуватися з PostgreSQL. Якщо тип стовпця bytea, то має використовуватись функція [pg\_escape\_bytea()](function.pg-escape-bytea.html) замість pgescapestring. Функція [pg\_escape\_identifier()](function.pg-escape-identifier.html) використовується для екранування ідентифікаторів (наприклад, імена таблиць або полів).

> **Зауваження**
> 
> Функція підтримується PostgreSQL версії 7.2 та вище.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Вихідний рядок, що екранується.

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_escape\_bytea()](function.pg-escape-bytea.html) - Екранує спецсимволи у рядку для вставки у поле типу bytea