---
navigation:
  - function.pg-lo-truncate.md: « pg\_lo\_truncate
  - function.pg-lo-write.md: pg\_lo\_write »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_unlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_unlink

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_unlink — Видалення великого об'єкта

### Опис

```methodsynopsis
pg_lo_unlink(PgSql\Connection $connection, int $oid): bool
```

**pg\_lo\_unlink()** видаляє великий об'єкт із ідентифікатором `oid`

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_lounlink()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`oid`

OID великий об'єкт у базі даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_unlink()\*\*\*\*

```php
<?php
   // OID удаляемого объекта
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   pg_lo_unlink($database, $doc_oid);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [pg\_lo\_create()](function.pg-lo-create.md) \- Створює великий об'єкт
-   [pg\_lo\_import()](function.pg-lo-import.md) \- Імпорт великого об'єкта з файлу
