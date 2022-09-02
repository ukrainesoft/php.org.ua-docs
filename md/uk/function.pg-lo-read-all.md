---
navigation:
  - function.pg-lo-open.md: « pgлоopen
  - function.pg-lo-read.md: пглоread »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пглоreadall
---
# пглоreadall

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоreadall — Читає вміст великого об'єкта і надсилає його безпосередньо до браузера.

### Опис

```methodsynopsis
pg_lo_read_all(PgSql\Lob $lob): int
```

**пглоreadall()** читає великий об'єкт і надсилає дані безпосередньо в браузер після відправлення всіх необхідних заголовків. Використовується в основному для пересилання бінарних даних, таких як зображення або звук.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloreadall()**

### Список параметрів

`lob`

Ан [PgSqlLob](class.pgsql-lob.md) instance, returned by [пглоopen()](function.pg-lo-open.md)

### Значення, що повертаються

Кількість прочитаних байт.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пглоreadall()****

```php
<?php
   header('Content-type: image/jpeg');
   $image_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $image_oid, "r");
   pg_lo_read_all($handle);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [пглоread()](function.pg-lo-read.md) - Читає дані великого об'єкту
