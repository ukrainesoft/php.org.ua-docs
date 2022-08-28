Скасує групу запитів

-   [« eio\_grp\_add](function.eio-grp-add.html)
    
-   [eio\_grp\_limit »](function.eio-grp-limit.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
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

Вказівник на групу запитів, повернутий [eio\_grp()](function.eio-grp.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eio\_grp()](function.eio-grp.html) - Створює групу запитів
-   [eio\_grp\_add()](function.eio-grp-add.html) - Додає запит до групи запитів