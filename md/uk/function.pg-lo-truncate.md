---
navigation:
  - function.pg-lo-tell.md: « pg\_lo\_tell
  - function.pg-lo-unlink.md: pg\_lo\_unlink »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_truncate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_truncate

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

pg\_lo\_truncate — Обрізає великий об'єкт

### Опис

```methodsynopsis
pg_lo_truncate(PgSql\Lob $lob, int $size): bool
```

**pg\_lo\_truncate()** обрізає екземпляр [PgSql\\Lob](class.pgsql-lob.md)

Для використання інтерфейсу великого об'єкта необхідно укласти його в блок транзакцій.

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

`size`

Кількість байт для обрізання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_truncate()\*\*\*\*

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Обрезать до 0
   pg_lo_truncate($handle, 0);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [pg\_lo\_tell()](function.pg-lo-tell.md) \- Повертає поточне положення внутрішнього покажчика великого об'єкта
