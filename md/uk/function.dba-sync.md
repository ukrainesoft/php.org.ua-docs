Синхронізує базу даних

-   [« dba\_replace](function.dba-replace.html)
    
-   [ODBC »](book.uodbc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
-   Синхронізує базу даних
    

# dbasync

(PHP 4, PHP 5, PHP 7, PHP 8)

dbasync — Синхронізує базу даних

### Опис

```methodsynopsis
dba_sync(resource $dba): bool
```

**dbasync()** синхронізує базу даних. Швидше за все, якщо підтримується ця функція, викличе запис на диск.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_optimize()](function.dba-optimize.html) - Оптимізує базу даних