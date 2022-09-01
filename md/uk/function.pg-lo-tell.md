---
navigation:
  - function.pg-lo-seek.html: « pgлоseek
  - function.pg-lo-truncate.html: пглоtruncate »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоtell
---
# пглоtell

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоtell — Повертає поточне положення внутрішнього покажчика великого об'єкта

### Опис

```methodsynopsis
pg_lo_tell(PgSql\Lob $lob): int
```

**пглоtell()** повертає поточну позицію (відступ від початку) внутрішнього покажчика великого об'єкта.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

### Список параметрів

`lob`

Ан [PgSqlLob](class.pgsql-lob.html) instance, returned by [пглоopen()](function.pg-lo-open.html)

### Значення, що повертаються

Поточна позиція внутрішнього покажчика (кількість байт від початку) великого об'єкта. У разі помилки функція поверне негативне значення.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пглоtell()****

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Пропустить первые 50000 байт
   pg_lo_seek($handle, 50000, PGSQL_SEEK_SET);
   // Проверим, на сколько мы отступили
   $offset = pg_lo_tell($handle);
   echo "Текущее положение внутреннего указателя: $offset";
   pg_query($database, "commit");
?>
```

Результат виконання цього прикладу:

```
Текущее положение внутреннего указателя: 50000
```

### Дивіться також

-   [пглоseek()](function.pg-lo-seek.html) - Переміщує внутрішній покажчик великого об'єкта
