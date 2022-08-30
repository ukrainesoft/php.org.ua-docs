Закриває з'єднання ODBC

-   [« odbccloseall](function.odbc-close-all.html)
    
-   [odbccolumnprivileges »](function.odbc-columnprivileges.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Закриває з'єднання ODBC
    

# odbcclose

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcclose — Закриває з'єднання ODBC

### Опис

```methodsynopsis
odbc_close(resource $odbc): void
```

Закриває з'єднання із сервером бази даних.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.