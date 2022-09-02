---
navigation:
  - function.pg-lo-unlink.md: « pgлоunlink
  - function.pg-meta-data.md: пгmetadata »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоwrite
---
# пглоwrite

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоwrite — Записує дані у великий об'єкт

### Опис

```methodsynopsis
pg_lo_write(PgSql\Lob $lob, string $data, ?int $length = null): int|false
```

**пглоwrite()** записує дані у великий об'єкт, починаючи з поточної позиції внутрішнього покажчика.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгlowrite()**

### Список параметрів

`lob`

Ан [PgSqlLob](class.pgsql-lob.md) instance, returned by [пглоopen()](function.pg-lo-open.md)

`data`

Дані для запису на великий об'єкт. Якщо аргумент `length` заданий та менше розміру `data`, то записані будуть тільки `length` байт.

`length`

Необов'язковий аргумент. Максимальна кількість байт, що записуються. Має бути більше нуля і не перевищувати розмір `data`. За замовчуванням приймається рівним розміром `data`

### Значення, що повертаються

Кількість записаних у великий об'єкт байт, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пглоwrite()****

```php
<?php
   $doc_oid = 189762345;
   $data = "This will overwrite the start of the large object.";
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "w");
   $data = pg_lo_write($handle, $data);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [пглоcreate()](function.pg-lo-create.md) - Створює великий об'єкт
-   [пглоopen()](function.pg-lo-open.md) - Відкриває великий об'єкт бази даних
