Читає дані великого об'єкту

-   [« pgлоreadall](function.pg-lo-read-all.html)
    
-   [пглоseek »](function.pg-lo-seek.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Читає дані великого об'єкту
    

# пглоread

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пглоread — Читає дані великого об'єкту

### Опис

```methodsynopsis
pg_lo_read(PgSql\Lob $lob, int $length = 8192): string|false
```

**пглоread()** читає `length` байт великого об'єкта та повертає їх у вигляді рядка.

Операції з використанням інтерфейсу великих об'єктів необхідно укладати у блок транзакції.

> **Зауваження**
> 
> Колишня назва функції: **пгloread()**

### Список параметрів

`length`

Ан [PgSqlLob](class.pgsql-lob.html) instance, returned by [пглоopen()](function.pg-lo-open.html)

`length`

Необов'язковий аргумент. Кількість байт, які потрібно прочитати.

### Значення, що повертаються

Рядок(string), що містить `length` байт великого об'єкта, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `lob` тепер чекає екземпляр [PgSqlLob](class.pgsql-lob.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пглоread()****

```php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   $data = pg_lo_read($handle, 50000);
   pg_query($database, "commit");
   echo $data;
?>
```

### Дивіться також

-   [пглоreadall()](function.pg-lo-read-all.html) - Читає вміст великого об'єкта та посилає безпосередньо до браузера