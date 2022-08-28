Обрізає великий об'єкт

-   [« pg\_lo\_tell](function.pg-lo-tell.html)
    
-   [pg\_lo\_unlink »](function.pg-lo-unlink.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Обрізає великий об'єкт
    

# пглоtruncate

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пглоtruncate — Обрізає великий об'єкт

### Опис

```methodsynopsis
pg_lo_truncate(PgSql\Lob $lob, int $size): bool
```

**пглоtruncate()** обрізає екземпляр [PgSql\\Lob](class.pgsql-lob.html)

Для використання інтерфейсу великого об'єкта необхідно укласти його в блок транзакцій.

### Список параметрів

`lob`

Ан [PgSql\\Lob](class.pgsql-lob.html) instance, returned by [pg\_lo\_open()](function.pg-lo-open.html)

`size`

Кількість байт для обрізання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                    |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `lob` тепер чекає екземпляр [PgSql\\Lob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_lo\_tell()](function.pg-lo-tell.html) - Повертає поточне положення внутрішнього покажчика великого об'єкта