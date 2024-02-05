---
navigation:
  - function.pg-lo-read-all.md: « pg\_lo\_read\_all
  - function.pg-lo-seek.md: pg\_lo\_seek »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_read

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_read — Читає дані великого об'єкту

### Опис

```methodsynopsis
pg_lo_read(PgSql\Lob $lob, int $length = 8192): string|false
```

**pg\_lo\_read()** читає `length` байт великого об'єкта та повертає їх у вигляді рядка.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loread()**

### Список параметрів

`length`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

`length`

Необов'язковий аргумент. Кількість байт, які потрібно прочитати.

### Значення, що повертаються

Рядок(string), що містить `length` байт великого об'єкта, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_read()\*\*\*\*

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   $data = pg_lo_read($handle, 50000);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [pg\_lo\_read\_all()](function.pg-lo-read-all.md) \- Читає вміст великого об'єкта та посилає безпосередньо до браузера
