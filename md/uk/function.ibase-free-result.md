Звільняє набір результатів

-   [« ibase\_free\_query](function.ibase-free-query.html)
    
-   [ibase\_gen\_id »](function.ibase-gen-id.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Звільняє набір результатів
    

# ibasefreeresult

(PHP 5, PHP 7 < 7.4.0)

ibasefreeresult — Звільняє набір результатів

### Опис

```methodsynopsis
ibase_free_result(resource $result_identifier): bool
```

Звільняє набір результатів.

### Список параметрів

`result_identifier`

Набір результатів, створених за допомогою [ibase\_query()](function.ibase-query.html) або [ibase\_execute()](function.ibase-execute.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.