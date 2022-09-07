---
navigation:
  - function.pg-lo-export.md: « pgлоexport
  - function.pg-lo-open.md: пглоopen »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоimport
---
# пглоimport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоimport — імпорт великого об'єкта з файлу

### Опис

```methodsynopsis
pg_lo_import(PgSql\Connection $connection = ?, string $pathname, mixed $object_id = ?): int
```

**пглоimport()** створює великий об'єкт у базі даних, використовуючи локальний файл як джерело даних.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloimport()**

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`pathname`

Повний шлях та ім'я файлу у клієнтській файловій системі для читання даних великого об'єкта.

`object_id`

Якщо заданий аргумент `object_id`, функція спробує створити об'єкт із цим ідентифікатором, інакше буде використано вільний ідентифікатор, призначений сервером. Цей аргумент ґрунтується на функціоналі, вперше реалізованому в PostgreSQL 8.1.

### Значення, що повертаються

OID створеного великого об'єкта або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пглоimport()****

```php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_import($database, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [пглоexport()](function.pg-lo-export.md) - Виведення великого об'єкта у файл
-   [пглоopen()](function.pg-lo-open.md) - Відкриває великий об'єкт бази даних
