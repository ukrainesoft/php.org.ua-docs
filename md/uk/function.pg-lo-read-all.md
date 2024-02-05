---
navigation:
  - function.pg-lo-open.md: « pg\_lo\_open
  - function.pg-lo-read.md: pg\_lo\_read »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_lo\_read\_all
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_lo\_read\_all

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_lo\_read\_all — Читає вміст великого об'єкта і надсилає його безпосередньо до браузера.

### Опис

```methodsynopsis
pg_lo_read_all(PgSql\Lob $lob): int
```

**pg\_lo\_read\_all()** читає великий об'єкт і надсилає дані безпосередньо в браузер після відправлення всіх необхідних заголовків. Використовується в основному для пересилання бінарних даних, таких як зображення або звук.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_loreadall()**

### Список параметрів

`lob`

An[PgSql\\Lob](class.pgsql-lob.md)instance, returned by[pg\_lo\_open()](function.pg-lo-open.md)

### Значення, що повертаються

Кількість прочитаних байт.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_lo\_read\_all()\*\*\*\*

```php
<?php
   header('Content-type: image/jpeg');
   $image_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $image_oid, "r");
   pg_lo_read_all($handle);
   pg_query($database, "commit");
?>
```

### Дивіться також

-   [pg\_lo\_read()](function.pg-lo-read.md) \- Читає дані великого об'єкту
