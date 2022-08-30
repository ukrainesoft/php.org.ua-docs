Витягує перший ключ

-   [« dbafetch](function.dba-fetch.html)
    
-   [dbahandlers »](function.dba-handlers.html)
    
-   [PHP Manual](index.html)
    
-   [Функції DBA](ref.dba.html)
    
-   Витягує перший ключ
    

# dbafirstkey

(PHP 4, PHP 5, PHP 7, PHP 8)

dbafirstkey — Витягує перший ключ

### Опис

```methodsynopsis
dba_firstkey(resource $dba): string|false
```

**dbafirstkey()** повертає перший ключ із бази даних і скидає внутрішній покажчик. Це дозволяє робити прямий пошук по всій базі.

### Список параметрів

`dba`

Обробник бази даних, повернутий [dbaopen()](function.dba-open.html) або [dbapopen()](function.dba-popen.html)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dbanextkey()](function.dba-nextkey.html) - Витягує наступний ключ
-   [dbakeysplit()](function.dba-key-split.html) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у [приклади DBA](dba.examples.html)