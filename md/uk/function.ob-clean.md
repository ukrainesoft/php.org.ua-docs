---
navigation:
  - function.flush.md: « flush
  - function.ob-end-clean.html: проendclean »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проclean
---
# проclean

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проclean — Очистити (стерти) буфер виводу

### Опис

```methodsynopsis
ob_clean(): bool
```

Ця функція очищає вміст вихідного буфера, не надсилаючи його до браузера.

Ця функція не знищує буфер виводу, як це робить [проendclean()](function.ob-end-clean.md)

Буфер виводу має запускатися функцією [проstart()](function.ob-start.md) з прапором [PHPOUTPUTHANDLERCLEANABLE](outcontrol.constants.html#constant.php-output-handler-cleanable). Інакше **проclean()** не спрацює.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [проflush()](function.ob-flush.md) - Скинути (надіслати) буфер виводу
-   [проendflush()](function.ob-end-flush.md) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [проendclean()](function.ob-end-clean.md) - Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
