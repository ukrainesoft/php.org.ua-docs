Перевірка з'єднання з базою даних

-   [« pg\_pconnect](function.pg-pconnect.html)
    
-   [pg\_port »](function.pg-port.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Перевірка з'єднання з базою даних
    

# пгping

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгping — Перевірити з'єднання з базою даних

### Опис

```methodsynopsis
pg_ping(?PgSql\Connection $connection = null): bool
```

**пгping()** перевіряє з'єднання з базою даних та перепідключається, якщо воно порушено.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгping()****

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

if (!pg_ping($conn))
  die("Соединение нарушено\n");
?>
```

### Дивіться також

-   [pg\_connection\_status()](function.pg-connection-status.html) - Визначає стан підключення
-   [pg\_connection\_reset()](function.pg-connection-reset.html) - Скидання підключення (перепідключення)