Відкочує транзакцію

-   [« odbcresult](function.odbc-result.html)
    
-   [odbcsetoption »](function.odbc-setoption.html)
    
-   [PHP Manual](index.md)
    
-   [Функции ODBC](ref.uodbc.md)
    
-   Відкочує транзакцію
    

# odbcrollback

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcrollback - Відкочує транзакцію

### Опис

```methodsynopsis
odbc_rollback(resource $odbc): bool
```

Відкочує всі незавершені операції у з'єднанні.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, див. [odbcconnect()](function.odbc-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.