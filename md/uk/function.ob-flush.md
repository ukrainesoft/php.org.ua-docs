---
navigation:
  - function.ob-end-flush.md: « obendflush
  - function.ob-get-clean.md: проgetclean »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проflush
---
# проflush

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проflush — Скинути (надіслати) буфер виводу

### Опис

```methodsynopsis
ob_flush(): bool
```

Ця функція надішле вміст буфера виводу (якщо є). Якщо необхідна подальша обробка буфера виводу, слід викликати [проgetcontents()](function.ob-get-contents.md) перед **проflush()**, оскільки вміст буфера буде видалено після виклику **проflush()**

Ця функція не знищує буфер виводу, як це робить [проendflush()](function.ob-end-flush.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [проgetcontents()](function.ob-get-contents.md) - Повертає вміст буфера виводу
-   [проclean()](function.ob-clean.md) - Очистити (стерти) буфер виводу
-   [проendflush()](function.ob-end-flush.md) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [проendclean()](function.ob-end-clean.md) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
