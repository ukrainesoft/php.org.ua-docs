---
navigation:
  - function.pg-lo-unlink.md: « pg\_lo\_unlink
  - function.pg-meta-data.md: pg\_meta\_data »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_write

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_write — Записує дані у великий об'єкт

### Опис

```methodsynopsis
pg_lo_write(PgSql\Lob $lob, string $data, ?int $length = null): int|false
```

**pg\_lo\_write()** записує дані у великий об'єкт, починаючи з поточної позиції внутрішнього покажчика.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_lowrite()**

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

`data`

Дані для запису на великий об'єкт. Якщо аргумент `length` заданий та менше розміру `data`, то записані будуть тільки `length`байт.

`length`

Необов'язковий аргумент. Максимальна кількість байт, що записуються. Має бути більше нуля і не перевищувати розмір `data`. За замовчуванням приймається рівним розміром `data`

### Значення, що повертаються

Кількість записаних у великий об'єкт байт, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `length` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_lo\_write()\*\*\*\*

```php
<?php
   $doc_oid = 189762345;
   $data = "This will overwrite the start of the large object.";
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "w");
   $data = pg_lo_write($handle, $data);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [pg\_lo\_create()](function.pg-lo-create.md) \- Створює великий об'єкт
-   [pg\_lo\_open()](function.pg-lo-open.md) \- Відкриває великий об'єкт бази даних
