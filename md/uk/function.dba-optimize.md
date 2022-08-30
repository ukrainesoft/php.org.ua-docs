Оптимізує базу даних

-   [« dbaopen](function.dba-open.html)
    
-   [dbapopen »](function.dba-popen.html)
    
-   [PHP Manual](index.html)
    
-   [Функції DBA](ref.dba.html)
    
-   Оптимізує базу даних
    

# dbaoptimize

(PHP 4, PHP 5, PHP 7, PHP 8)

dbaoptimize - Оптимізує базу даних

### Опис

```methodsynopsis
dba_optimize(resource $dba): bool
```

**dbaoptimize()** оптимізує основну базу даних

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbasync()](function.dba-sync.html) - Синхронізує базу даних