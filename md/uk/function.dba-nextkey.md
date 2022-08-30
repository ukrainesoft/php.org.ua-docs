Витягує наступний ключ

-   [« dbalist](function.dba-list.html)
    
-   [dbaopen »](function.dba-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функції DBA](ref.dba.html)
    
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

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbafirstkey()](function.dba-firstkey.html) - Витягує перший ключ
-   [dbakeysplit()](function.dba-key-split.html) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у [приклади DBA](dba.examples.html)