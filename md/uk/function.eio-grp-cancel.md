Скасує групу запитів

-   [« eiogrpadd](function.eio-grp-add.html)
    
-   [eiogrplimit »](function.eio-grp-limit.html)
    
-   [PHP Manual](index.md)
    
-   [Eio Функции](ref.eio.md)
    
-   Скасує групу запитів
    

# eiogrpcancel

(PECL eio >= 0.0.1dev)

eiogrpcancel — Скасує групу запитів

### Опис

```methodsynopsis
eio_grp_cancel(resource $grp): void
```

**eiogrpcancel()** скасовує групу запитів, покажчик на яку визначено в `grp`

### Список параметрів

`grp`

Вказівник на групу запитів, повернутий [eiogrp()](function.eio-grp.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eiogrp()](function.eio-grp.html) - Створює групу запитів
-   [eiogrpadd()](function.eio-grp-add.html) - Додає запит до групи запитів