Оптимізує базу даних

-   [« dba\_open](function.dba-open.html)
    
-   [dba\_popen »](function.dba-popen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
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

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_sync()](function.dba-sync.html) - Синхронізує базу даних