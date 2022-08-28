Повертає кількість стовпців у результаті

-   [« odbc\_next\_result](function.odbc-next-result.html)
    
-   [odbc\_num\_rows »](function.odbc-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає кількість стовпців у результаті
    

# odbcnumfields

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcnumfields — Повертає кількість стовпців у результаті

### Опис

```methodsynopsis
odbc_num_fields(resource $statement): int
```

Повертає кількість полів (стовпців) у результаті ODBC.

### Список параметрів

`statement`

Ідентифікатор результату, що повертається [odbc\_exec()](function.odbc-exec.html)

### Значення, що повертаються

Повертає кількість полів або -1 у разі помилки.