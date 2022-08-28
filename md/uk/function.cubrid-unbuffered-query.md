Виконання запиту без завантаження результату на згадку

-   [« cubrid\_result](function.cubrid-result.html)
    
-   [Устаревшие псевдонимы и функции CUBRID »](oldaliases.cubrid.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Виконання запиту без завантаження результату на згадку
    

# cubridunbufferedquery

(PECL CUBRID >= 8.3.0)

cubridunbufferedquery — Виконання запиту без завантаження результату на згадку

### Опис

```methodsynopsis
cubrid_unbuffered_query(string $query, resource $conn_identifier = ?): resource
```

Функція виконує запит без очікування на його виконання. Вона повертає значення у процесі створення результуючого набору.

### Список параметрів

`query`

SQL-запит

`conn_identifier`

Ідентифікатор з'єднання CUBRID. Якщо не встановлено, то буде використано останнє з'єднання, повернене [cubrid\_connect()](function.cubrid-connect.html)

### Значення, що повертаються

Для SELECT, SHOW, DESCRIBE, EXPLAIN та інших запитів, що повертають результуючий набір, [cubrid\_query()](function.cubrid-query.html) повертає ресурс у разі успішного виконання.

Для операторів SQL іншого типу UPDATE, DELETE, DROP і т.д. повертає **`true`** у разі успішного виконання.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridunbufferedquery()****

```php
<?php
    $link = cubrid_connect("localhost", 30000, "demodb", "dba", "");
    if (!$link)
    {
        die('Не удалось соединиться.');
    }
    $query = "select * from code";
    $result = cubrid_unbuffered_query($query, $link);

    while ($row = cubrid_fetch($result))
    {
        var_dump($row);
    }

    cubrid_close_request($result);
    cubrid_disconnect($link);
?>
```

### Примітки

> **Зауваження**
> 
> Переваги **cubridunbufferedquery()** мають свою ціну: ви не зможете використати [cubrid\_num\_rows()](function.cubrid-num-rows.html) і [cubrid\_data\_seek()](function.cubrid-data-seek.html) для результуючого набору, повернутий **cubridunbufferedquery()**