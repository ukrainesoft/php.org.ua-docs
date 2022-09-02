---
navigation:
  - function.pg-lo-tell.md: « pgлоtell
  - function.pg-lo-unlink.md: пглоunlink »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоtruncate
---
# пглоtruncate

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пглоtruncate — Обрізає великий об'єкт

### Опис

```methodsynopsis
pg_lo_truncate(PgSql\Lob $lob, int $size): bool
```

**пглоtruncate()** обрізає екземпляр [PgSqlLob](class.pgsql-lob.md)

Для використання інтерфейсу великого об'єкта необхідно укласти його в блок транзакцій.

### Список параметрів

`lob`

Ан [PgSqlLob](class.pgsql-lob.md) instance, returned by [пглоopen()](function.pg-lo-open.md)

`size`

Кількість байт для обрізання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пглоtruncate()****

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Обрезать до 0
   pg_lo_truncate($handle, 0);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [пглоtell()](function.pg-lo-tell.md) - Повертає поточне положення внутрішнього покажчика великого об'єкта
