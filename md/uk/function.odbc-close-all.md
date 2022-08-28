Закриває всі з'єднання ODBC

-   [« odbc\_binmode](function.odbc-binmode.html)
    
-   [odbc\_close »](function.odbc-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Закриває всі з'єднання ODBC
    

# odbccloseall

(PHP 4, PHP 5, PHP 7, PHP 8)

odbccloseall — Закриває всі з'єднання ODBC

### Опис

```methodsynopsis
odbc_close_all(): void
```

**odbccloseall()** закриє всі з'єднання із сервером (серверами) бази даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Примітки

> **Зауваження**
> 
> Ця функція не спрацює, якщо з'єднання є відкритими транзакціями. У цьому випадку з'єднання залишиться відкритим.