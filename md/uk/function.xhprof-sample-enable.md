---
navigation:
  - function.xhprof-sample-disable.md: « xhprofsampledisable
  - book.yac.md: Yac »
  - index.md: PHP Manual
  - ref.xhprof.md: Функции Xhprof
title: xhprofsampleenable
---
# xhprofsampleenable

(PECL xhprof >= 0.9.0)

xhprofsampleenable — Запуск семплюючого режиму профілю XHProf

### Опис

```methodsynopsis
xhprof_sample_enable(): void
```

Запуск семплюючого режиму профілювання, що є полегшеною версією [xhprofenable()](function.xhprof-enable.md). Інтервал семплювання складає 0,1 секунди і при кожній ітерації записується стек викликів. Цей режим призначений для зниження накладних витрат під час моніторингу продуктивності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`null`**

### Дивіться також

-   [xhprofsampledisable()](function.xhprof-sample-disable.md) - Зупинити семплююче профіль xhprof
-   [xhprofenable()](function.xhprof-enable.md) - Запуск профілювання xhprof
-   [memorygetusage()](function.memory-get-usage.md) - Повертає кількість пам'яті, виділену для PHP
-   [getrusage()](function.getrusage.md) - Отримує інформацію про використання поточного ресурсу
