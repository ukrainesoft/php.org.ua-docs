Перегляд поточних значень параметрів сервера

-   [« pg\_options](function.pg-options.html)
    
-   [pg\_pconnect »](function.pg-pconnect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Перегляд поточних значень параметрів сервера
    

# пгparameterstatus

(PHP 5, PHP 7, PHP 8)

пгparameterstatus — Перегляд поточних значень параметрів сервера

### Опис

```methodsynopsis
pg_parameter_status(PgSql\Connection $connection = ?, string $param_name): string
```

Отримує поточне значення параметра сервера.

Значення деяких параметрів сервер автоматично повідомляється під час встановлення підключення або зміни даних. Функція **пгparameterstatus()** може вимагати подібні значення. Вона повертає значення параметра, якщо його визначено, або **`false`** у разі виникнення помилки.

Список параметрів серверів PostgreSQL версій 8.0 та вище: `server_version` `server_encoding` `client_encoding` `is_superuser` `session_authorization` `DateStyle` `TimeZone`, і `integer_datetimes`. `server_encoding` `TimeZone`, і `integer_datetimes` не визначаються для версій нижче 8.0.) `server_version` `server_encoding` і `integer_datetimes` не можна змінити після запуску PostgreSQL.

Незважаючи на те, що PostgreSQL версій 7.3 і нижче не повідомляють значень своїх параметрів, **пгparameterstatus()** дозволяє визначити значення параметрів `server_version` і `client_encoding`. Для визначення значень цих параметрів краще використовувати **пгparameterstatus()**, ніж спеціально розробляти інші функції.

**Застереження**

Якщо під час використання сервера PostgreSQL версій 7.4 і нижче змінити параметр `client_encoding` за допомогою команди сервера `SET` вже після встановлення з'єднання, функція **пгparameterstatus()** не зможе відобразити цей факт.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`param_name`

Допустимі значення аргументу: `server_version` `server_encoding` `client_encoding` `is_superuser` `session_authorization` `DateStyle` `TimeZone` і `integer_datetimes`. Зверніть увагу, що це значення чутливе до регістру.

### Значення, що повертаються

Значення запитуваного параметра у вигляді рядка, або **`false`**, якщо передано неприпустимий параметр.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгparameterstatus()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с сервером");

  echo "Кодировка сервера: ", pg_parameter_status($dbconn, "server_encoding");
?>
```

Результат виконання цього прикладу:

```
Кодировка сервера: SQL_ASCII
```