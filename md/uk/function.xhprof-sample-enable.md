Запуск семплюючого режиму профілювання XHProf

-   [« xhprof\_sample\_disable](function.xhprof-sample-disable.html)
    
-   [Yac »](book.yac.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Xhprof](ref.xhprof.html)
    
-   Запуск семплюючого режиму профілювання XHProf
    

# xhprofsampleenable

(PECL xhprof >= 0.9.0)

xhprofsampleenable — Запуск семплюючого режиму профілю XHProf

### Опис

```methodsynopsis
xhprof_sample_enable(): void
```

Запуск семплюючого режиму профілювання, що є полегшеною версією [xhprof\_enable()](function.xhprof-enable.html). Інтервал семплювання складає 0,1 секунди і при кожній ітерації записується стек викликів. Цей режим призначений для зниження накладних витрат під час моніторингу продуктивності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`null`**

### Дивіться також

-   [xhprof\_sample\_disable()](function.xhprof-sample-disable.html) - Зупинити семплююче профіль xhprof
-   [xhprof\_enable()](function.xhprof-enable.html) - Запуск профілювання xhprof
-   [memory\_get\_usage()](function.memory-get-usage.html) - Повертає кількість пам'яті, виділену для PHP
-   [getrusage()](function.getrusage.html) - Отримує інформацію про використання поточного ресурсу