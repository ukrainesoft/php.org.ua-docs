---
navigation:
  - function.pg-lo-read.md: « pg\_lo\_read
  - function.pg-lo-tell.md: pg\_lo\_tell »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_seek

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_seek — Переміщує внутрішній вказівник великого об'єкта

### Опис

```methodsynopsis
pg_lo_seek(PgSql\Lob $lob, int $offset, int $whence = SEEK_CUR): bool
```

**pg\_lo\_seek()** переміщує внутрішній покажчик екземпляра [PgSql\\Lob](class.pgsql-lob.md)

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

`offset`

Кількість байт, скільки потрібно перемістити покажчик.

`whence`

Одна из констант:**`PGSQL_SEEK_SET`** (переміщати від початку об'єкта), **`PGSQL_SEEK_CUR`** (переміщати з поточної позиції) або **`PGSQL_SEEK_END`** (Відступати від кінця об'єкта).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_lo\_seek()\*\*\*\*

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Пропустить первые 50000 байт
   pg_lo_seek($handle, 50000, PGSQL_SEEK_SET);
   // Прочитать следующие 10000 байт
   $data = pg_lo_read($handle, 10000);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [pg\_lo\_tell()](function.pg-lo-tell.md) \- Повертає поточне положення внутрішнього покажчика великого об'єкта
