Фіксує транзакцію ODBC

-   [« odbc\_columns](function.odbc-columns.html)
    
-   [odbc\_connect »](function.odbc-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Фіксує транзакцію ODBC
    

# odbccommit

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccommit - Фіксує транзакцію ODBC

### Опис

```methodsynopsis
odbc_commit(resource $odbc): bool
```

Фіксує всі незавершені транзакції з'єднання.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbc\_connect()](function.odbc-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.