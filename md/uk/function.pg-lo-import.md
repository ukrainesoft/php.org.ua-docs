---
navigation:
  - function.pg-lo-export.md: « pg\_lo\_export
  - function.pg-lo-open.md: pg\_lo\_open »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_import

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_import — імпорт великого об'єкта з файлу

### Опис

```methodsynopsis
pg_lo_import(PgSql\Connection $connection = ?, string $pathname, mixed $object_id = ?): int
```

**pg\_lo\_import()** створює великий об'єкт у базі даних, використовуючи локальний файл як джерело даних.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loimport()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`pathname`

Повний шлях та ім'я файлу у клієнтській файловій системі для читання даних великого об'єкта.

`object_id`

Если задан аргумент`object_id`, функція спробує створити об'єкт із цим ідентифікатором, інакше буде використано вільний ідентифікатор, призначений сервером. Цей аргумент ґрунтується на функціоналі, вперше реалізованому в PostgreSQL 8.1.

### Значення, що повертаються

OID створеного великого об'єкта або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_import()\*\*\*\*

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_import($database, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [pg\_lo\_export()](function.pg-lo-export.md) \- Виведення великого об'єкта у файл
-   [pg\_lo\_open()](function.pg-lo-open.md) \- Відкриває великий об'єкт бази даних
