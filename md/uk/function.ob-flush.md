---
navigation:
  - function.ob-end-flush.html: « obendflush
  - function.ob-get-clean.html: проgetclean »
  - index.html: PHP Manual
  - ref.outcontrol.html: Функції контролю виведення
title: проflush
---
# проflush

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проflush — Скинути (надіслати) буфер виводу

### Опис

```methodsynopsis
ob_flush(): bool
```

Ця функція надішле вміст буфера виводу (якщо є). Якщо необхідна подальша обробка буфера виводу, слід викликати [проgetcontents()](function.ob-get-contents.html) перед **проflush()**, оскільки вміст буфера буде видалено після виклику **проflush()**

Ця функція не знищує буфер виводу, як це робить [проendflush()](function.ob-end-flush.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [проgetcontents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [проclean()](function.ob-clean.html) - Очистити (стерти) буфер виводу
-   [проendflush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [проendclean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
