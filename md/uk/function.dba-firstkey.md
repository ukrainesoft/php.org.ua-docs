Витягує перший ключ

-   [« dba\_fetch](function.dba-fetch.html)
    
-   [dba\_handlers »](function.dba-handlers.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DBA](ref.dba.html)
    
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

Обробник бази даних, повернутий [dba\_open()](function.dba-open.html) або [dba\_popen()](function.dba-popen.html)

### Значення, що повертаються

Повертає ключ у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [dba\_nextkey()](function.dba-nextkey.html) - Витягує наступний ключ
-   [dba\_key\_split()](function.dba-key-split.html) - Розділяє ключ, заданий у вигляді рядка та створює масив з отриманих частин
-   Другий приклад у [примерах DBA](dba.examples.html)