Повертає ім'я курсору

-   [« odbcconnect](function.odbc-connect.html)
    
-   [odbcdatasource »](function.odbc-data-source.html)
    
-   [PHP Manual](index.md)
    
-   [Функции ODBC](ref.uodbc.md)
    
-   Повертає ім'я курсору
    

# odbccursor

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccursor — Повертає ім'я курсору

### Опис

```methodsynopsis
odbc_cursor(resource $statement): string|false
```

Повертає ім'я курсору для даного resultid.

### Список параметрів

`statement`

Ідентифікатор результату.

### Значення, що повертаються

Повертає ім'я курсора у вигляді рядка або **`false`** у разі виникнення помилки.