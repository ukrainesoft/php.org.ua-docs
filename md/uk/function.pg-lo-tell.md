---
navigation:
  - function.pg-lo-seek.md: « pg\_lo\_seek
  - function.pg-lo-truncate.md: pg\_lo\_truncate »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_tell
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_tell

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_tell — Повертає поточне положення внутрішнього покажчика великого об'єкта

### Опис

```methodsynopsis
pg_lo_tell(PgSql\Lob $lob): int
```

**pg\_lo\_tell()** повертає поточну позицію (відступ від початку) внутрішнього покажчика великого об'єкта.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

### Значення, що повертаються

Поточна позиція внутрішнього покажчика (кількість байт від початку) великого об'єкта. У разі помилки функція поверне негативне значення.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_tell()\*\*\*\*

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Пропустить первые 50000 байт
   pg_lo_seek($handle, 50000, PGSQL_SEEK_SET);
   // Проверим, на сколько мы отступили
   $offset = pg_lo_tell($handle);
   echo "Текущее положение внутреннего указателя: $offset";
   pg_query($database, "commit");
?>
```

Результат виконання наведеного прикладу:

```
Текущее положение внутреннего указателя: 50000
```

### Дивіться також

-   [pg\_lo\_seek()](function.pg-lo-seek.md) \- Переміщує внутрішній покажчик великого об'єкта
