Закриває базу даних DBA

-   [« Функції DBA](ref.dba.html)
    
-   [dbadelete »](function.dba-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функції DBA](ref.dba.html)
    
-   Закриває базу даних DBA
    

# dbaclose

(PHP 4, PHP 5, PHP 7, PHP 8)

dbaclose — Закриває базу даних DBA

### Опис

```methodsynopsis
dba_close(resource $dba): void
```

**dbaclose()** закриває встановлену базу даних та звільняє всі пов'язані з нею ресурси.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [dbaopen()](function.dba-open.html) - Відкриває базу даних
-   [dbapopen()](function.dba-popen.html) - встановити постійний екземпляр бази даних