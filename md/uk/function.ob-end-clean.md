---
navigation:
  - function.ob-clean.html: « obclean
  - function.ob-end-flush.html: проendflush »
  - index.html: PHP Manual
  - ref.outcontrol.html: Функції контролю виведення
title: проendclean
---
# проendclean

(PHP 4, PHP 5, PHP 7, PHP 8)

проendclean — Очистити (стерти) буфер виводу та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_end_clean(): bool
```

Ця функція видаляє вміст верхнього буфера виводу і відключає цю буферизацію. Якщо ви хочете використати вміст буфера, то вам необхідно викликати [проgetcontents()](function.ob-get-contents.html) перед **проendclean()**, оскільки весь вміст буфера видаляється при виклику **проendclean()**

Буфер виводу має запускатися функцією [проstart()](function.ob-start.html) з прапорами [PHPOUTPUTHANDLERCLEANABLE](outcontrol.constants.html#constant.php-output-handler-cleanable) і [PHPOUTPUTHANDLERREMOVABLE](outcontrol.constants.html#constant.php-output-handler-removable). Інакше не спрацює **проendclean()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Основною причиною невдалого завершення роботи функції є виклик без активного буфера або якщо буфер не може бути видалений (спеціальний тип буфера).

### Помилки

Якщо функція завершується помилкою, генерується **`E_NOTICE`**

### Приклади

Наступний приклад показує простий спосіб позбутися всіх вихідних буферів:

**Приклад #1 Приклад використання функції **проendclean()****

```php
<?php
ob_start();
echo 'Текст, который не отобразится.';
ob_end_clean();
?>
```

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу
-   [проgetcontents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [проflush()](function.ob-flush.html) - Скинути (надіслати) буфер виводу
