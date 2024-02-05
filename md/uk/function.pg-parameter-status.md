---
navigation:
  - function.pg-options.md: « pg\_options
  - function.pg-pconnect.md: pg\_pconnect »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_parameter\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_parameter\_status

(PHP 5, PHP 7, PHP 8)

pg\_parameter\_status — Перегляд поточних значень параметрів сервера

### Опис

```methodsynopsis
pg_parameter_status(PgSql\Connection $connection = ?, string $param_name): string
```

Отримує поточне значення параметра сервера.

Значення деяких параметрів сервер автоматично повідомляється під час встановлення підключення або зміни даних. Функція **pg\_parameter\_status()** може вимагати подібні значення. Вона повертає значення параметра, якщо його визначено, або \*\*`false`\*\*в случае возникновения ошибки.

Список параметрів серверів PostgreSQL версій 8.0 та вище: `server_version` `server_encoding` `client_encoding` `is_superuser` `session_authorization` `DateStyle` `TimeZone`, и`integer_datetimes`. `server_encoding` `TimeZone`, и`integer_datetimes` не визначаються для версій нижче 8.0.) `server_version` `server_encoding`и`integer_datetimes`нельзя изменить после запуска PostgreSQL.

Незважаючи на те, що PostgreSQL версій 7.3 і нижче не повідомляють значень своїх параметрів, **pg\_parameter\_status()** дозволяє визначити значення параметрів `server_version`и`client_encoding`. Для визначення значень цих параметрів краще використовувати **pg\_parameter\_status()**, ніж спеціально розробляти інші функції.

**Застереження**

Якщо під час використання сервера PostgreSQL версій 7.4 і нижче змінити параметр `client_encoding` за допомогою команди сервера `SET`уже после установки соединения, функция**pg\_parameter\_status()** не зможе відобразити цей факт.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`param_name`

Допустимі значення аргументу: `server_version` `server_encoding` `client_encoding` `is_superuser` `session_authorization` `DateStyle` `TimeZone`и`integer_datetimes`. Зверніть увагу, що це значення чутливе до регістру.

### Значення, що повертаються

Значення запитуваного параметра у вигляді рядка, або **`false`**, якщо передано неприпустимий параметр.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_parameter\_status()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с сервером");

  echo "Кодировка сервера: ", pg_parameter_status($dbconn, "server_encoding");
?>
```

Результат виконання наведеного прикладу:

```
Кодировка сервера: SQL_ASCII
```
