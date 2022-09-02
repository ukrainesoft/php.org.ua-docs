---
navigation:
  - function.ob-end-clean.md: « obendclean
  - function.ob-flush.md: проflush »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проendflush
---
# проendflush

(PHP 4, PHP 5, PHP 7, PHP 8)

проendflush — Скинути (надіслати) буфер виведення та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_end_flush(): bool
```

Ця функція надішле вміст найвищого буфера виводу (якщо воно є) і відключить цей буфер виводу. Якщо ви хочете використати вміст буфера, то вам необхідно викликати [проgetcontents()](function.ob-get-contents.md) перед **проendflush()**, т.к. весь вміст буфера видаляється під час виклику **проendflush()**

Буфер виводу має запускатися функцією [проstart()](function.ob-start.md) з прапорами [PHPOUTPUTHANDLERFLUSHABLE](outcontrol.constants.md#constant.php-output-handler-flushable) і [PHPOUTPUTHANDLERREMOVABLE](outcontrol.constants.md#constant.php-output-handler-removable)

> **Зауваження**: Ця функція аналогічна [проgetflush()](function.ob-get-flush.md), за винятком того, що [проgetflush()](function.ob-get-flush.md) повертає вміст буфера у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Основною причиною невдалого завершення роботи функції є виклик без активного буфера або якщо буфер не може бути видалений (спеціальний тип буфера).

### Помилки

Якщо функція завершується помилкою, генерується **`E_NOTICE`**

### Приклади

**Приклад #1 Приклад використання функції **проendflush()****

Наступний приклад показує простий спосіб скидання та завершення всіх буферів виведення:

```php
<?php
  while (@ob_end_flush());
?>
```

### Дивіться також

-   [проstart()](function.ob-start.md) - Включення буферизації виводу
-   [проgetcontents()](function.ob-get-contents.md) - Повертає вміст буфера виводу
-   [проgetflush()](function.ob-get-flush.md) - Скинути буфер виведення, повернути його у вигляді рядка та вимкнути буферизацію виводу
-   [проflush()](function.ob-flush.md) - Скинути (надіслати) буфер виводу
-   [проendclean()](function.ob-end-clean.md) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
