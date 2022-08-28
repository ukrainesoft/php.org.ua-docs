Закриває базу даних DBA

-   [« Функции DBA](ref.dba.html)
    
-   [dba\_delete »](function.dba-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
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

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [dba\_open()](function.dba-open.html) - Відкриває базу даних
-   [dba\_popen()](function.dba-popen.html) - встановити постійний екземпляр бази даних