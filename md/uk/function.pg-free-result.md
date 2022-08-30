Очищення результату запиту та звільнення пам'яті

-   [« pgflush](function.pg-flush.html)
    
-   [пгgetnotify »](function.pg-get-notify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Очищення результату запиту та звільнення пам'яті
    

# пгfreeresult

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfreeresult — Очищення результату запиту та звільнення пам'яті

### Опис

```methodsynopsis
pg_free_result(PgSql\Result $result): bool
```

**пгfreeresult()** звільняє пам'ять, зайняту екземпляром [PgSqlResult](class.pgsql-result.html)

Викликати цю функцію слід лише у разі нестачі пам'яті під час виконання скрипта. У будь-якому випадку пам'ять буде звільнено автоматично після закінчення роботи скрипту.

> **Зауваження**
> 
> Колишня назва функції: **пгfreeresult()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                           |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгfreeresult()****

```php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "Первое поле во второй строчке: ", $val, "\n";

pg_free_result($res);
?>
```

Результат виконання цього прикладу:

```
Первое поле во второй строчке: 2
```

### Дивіться також

-   [пгquery()](function.pg-query.html) - Виконує запит
-   [пгqueryparams()](function.pg-query-params.html) - Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
-   [пгexecute()](function.pg-execute.html) - Запускає виконання раніше підготовленого параметризованого запиту та чекає результату