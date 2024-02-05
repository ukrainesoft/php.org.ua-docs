---
navigation:
  - function.cubrid-result.md: « cubrid\_result
  - oldaliases.cubrid.md: Застарілі псевдоніми та функції CUBRID »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_unbuffered\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_unbuffered\_query

(PECL CUBRID >= 8.3.0)

cubrid\_unbuffered\_query — Виконання запиту без завантаження результату на згадку

### Опис

```methodsynopsis
cubrid_unbuffered_query(string $query, resource $conn_identifier = ?): resource
```

Функція виконує запит без очікування на його виконання. Вона повертає значення у процесі створення результуючого набору.

### Список параметрів

`query`

SQL-запит

`conn_identifier`

Ідентифікатор з'єднання CUBRID. Якщо не встановлено, то буде використано останнє з'єднання, повернене [cubrid\_connect()](function.cubrid-connect.md)

### Значення, що повертаються

Для SELECT, SHOW, DESCRIBE, EXPLAIN та інших запитів, що повертають результуючий набір, [cubrid\_query()](function.cubrid-query.md) повертає ресурс у разі успішного виконання.

Для операторів SQL іншого типу UPDATE, DELETE, DROP і т.д. повертає **`true`** у разі успішного виконання.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_unbuffered\_query()\*\*\*\*

```php
<?php
    $link = cubrid_connect("localhost", 30000, "demodb", "dba", "");
    if (!$link)
    {
        die('Не удалось соединиться.');
    }
    $query = "select * from code";
    $result = cubrid_unbuffered_query($query, $link);

    while ($row = cubrid_fetch($result))
    {
        var_dump($row);
    }

    cubrid_close_request($result);
    cubrid_disconnect($link);
?>
```

### Примітки

> **Зауваження** :
> 
> Преимущества**cubrid\_unbuffered\_query()** мають свою ціну: ви не зможете використати [cubrid\_num\_rows()](function.cubrid-num-rows.md) і [cubrid\_data\_seek()](function.cubrid-data-seek.md) для результуючого набору, повернутий **cubrid\_unbuffered\_query()**
