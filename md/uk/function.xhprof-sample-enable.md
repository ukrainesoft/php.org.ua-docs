---
navigation:
  - function.xhprof-sample-disable.md: « xhprof\_sample\_disable
  - book.yac.md: Yac »
  - index.md: PHP Manual
  - ref.xhprof.md: Функції Xhprof
title: xhprof\_sample\_enable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xhprof\_sample\_enable

(PECL xhprof >= 0.9.0)

xhprof\_sample\_enable — Запуск семплюючого режиму профілю XHProf

### Опис

```methodsynopsis
xhprof_sample_enable(): void
```

Запуск семплюючого режиму профілювання, що є полегшеною версією [xhprof\_enable()](function.xhprof-enable.md). Інтервал семплювання складає 0,1 секунди і при кожній ітерації записується стек викликів. Цей режим призначений для зниження накладних витрат під час моніторингу продуктивності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`null`**

### Дивіться також

-   [xhprof\_sample\_disable()](function.xhprof-sample-disable.md) \- Зупинити семплююче профіль xhprof
-   [xhprof\_enable()](function.xhprof-enable.md) \- Запуск профілювання xhprof
-   [memory\_get\_usage()](function.memory-get-usage.md) \- Повертає кількість пам'яті, виділеної для PHP
-   [getrusage()](function.getrusage.md) \- Отримує інформацію про використання поточного ресурсу
