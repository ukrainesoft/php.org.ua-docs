Витягує наступний ключ

-   [« dba\_list](function.dba-list.html)
    
-   [dba\_open »](function.dba-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
-   Витягує наступний ключ
    

# dbanextkey

(PHP 4, PHP 5, PHP 7, PHP 8)

dbanextkey — Витягує наступний ключ

### Опис

```methodsynopsis
dba_nextkey(resource $dba): string|false
```

**dbanextkey()** повертає наступний ключ із бази даних та переміщає внутрішній покажчик.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_firstkey()](function.dba-firstkey.html) - Витягує перший ключ
-   [dba\_key\_split()](function.dba-key-split.html) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у [примерах DBA](dba.examples.html)