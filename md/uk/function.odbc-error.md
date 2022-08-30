Повертає останній код помилки

-   [« odbcдо](function.odbc-do.html)
    
-   [odbcerrormsg »](function.odbc-errormsg.html)
    
-   [PHP Manual](index.html)
    
-   [Функции ODBC](ref.uodbc.html)
    
-   Повертає останній код помилки
    

# odbcerror

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

odbcerror — Повертає останній код помилки

### Опис

```methodsynopsis
odbc_error(?resource $odbc = null): string
```

Повертає шестизначний стан ODBC або порожній рядок, якщо помилок не виникло.

### Список параметрів

`odbc`

Ідентифікатор з'єднання ODBC, за подробицями звертайтесь до [odbcconnect()](function.odbc-connect.html)

### Значення, що повертаються

Якщо вказано параметр `odbc`, повертається останній стан цієї сполуки, інакше повертається останній стан будь-якої сполуки.

Ця функція повертає осмислене значення лише тоді, коли останній запит ODBC завершився невдало (тобто функція [odbcexec()](function.odbc-exec.html) повернула **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `odbc` тепер допускає значення null. |

### Дивіться також

-   [odbcerrormsg()](function.odbc-errormsg.html) - Повертає останнє повідомлення про помилку
-   [odbcexec()](function.odbc-exec.html) - Виконує інструкцію SQL безпосередньо