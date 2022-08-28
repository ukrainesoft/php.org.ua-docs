Закриває з'єднання ODBC

-   [« odbc\_close\_all](function.odbc-close-all.html)
    
-   [odbc\_columnprivileges »](function.odbc-columnprivileges.html)
    
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

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbc\_connect()](function.odbc-connect.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.