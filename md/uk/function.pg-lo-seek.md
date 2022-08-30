Переміщує внутрішній покажчик великого об'єкту

-   [« pgлоread](function.pg-lo-read.html)
    
-   [пглоtell »](function.pg-lo-tell.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Переміщує внутрішній покажчик великого об'єкту
    

# пглоseek

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоseek — Переміщує внутрішній покажчик великого об'єкта

### Опис

```methodsynopsis
pg_lo_seek(PgSql\Lob $lob, int $offset, int $whence = SEEK_CUR): bool
```

**пглоseek()** переміщує внутрішній покажчик екземпляра [PgSqlLob](class.pgsql-lob.html)

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

### Список параметрів

`lob`

Ан [PgSqlLob](class.pgsql-lob.html) instance, returned by [пглоopen()](function.pg-lo-open.html)

`offset`

Кількість байт, скільки потрібно перемістити покажчик.

`whence`

Одна з констант: **`PGSQL_SEEK_SET`** (переміщати від початку об'єкта), **`PGSQL_SEEK_CUR`** (переміщати з поточної позиції) або **`PGSQL_SEEK_END`** (Відступати від кінця об'єкта).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоseek()****

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Пропустить первые 50000 байт
   pg_lo_seek($handle, 50000, PGSQL_SEEK_SET);
   // Прочитать следующие 10000 байт
   $data = pg_lo_read($handle, 10000);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [пглоtell()](function.pg-lo-tell.html) - Повертає поточне положення внутрішнього покажчика великого об'єкта