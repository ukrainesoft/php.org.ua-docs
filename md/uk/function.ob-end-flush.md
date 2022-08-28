Скинути (надіслати) буфер виведення та вимкнути буферизацію виводу

-   [« ob\_end\_clean](function.ob-end-clean.html)
    
-   [ob\_flush »](function.ob-flush.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Скинути (надіслати) буфер виведення та вимкнути буферизацію виводу
    

# проendflush

(PHP 4, PHP 5, PHP 7, PHP 8)

проendflush — Скинути (надіслати) буфер виведення та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_end_flush(): bool
```

Ця функція надішле вміст найвищого буфера виводу (якщо воно є) і відключить цей буфер виводу. Якщо ви хочете використати вміст буфера, то вам необхідно викликати [ob\_get\_contents()](function.ob-get-contents.html) перед **проendflush()**, т.к. весь вміст буфера видаляється під час виклику **проendflush()**

Буфер виводу має запускатися функцією [ob\_start()](function.ob-start.html) з прапорами [PHP\_OUTPUT\_HANDLER\_FLUSHABLE](outcontrol.constants.html#constant.php-output-handler-flushable) і [PHP\_OUTPUT\_HANDLER\_REMOVABLE](outcontrol.constants.html#constant.php-output-handler-removable)

> **Зауваження**: Ця функція аналогічна [ob\_get\_flush()](function.ob-get-flush.html), за винятком того, що [ob\_get\_flush()](function.ob-get-flush.html) повертає вміст буфера у вигляді рядка.

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

-   [ob\_start()](function.ob-start.html) - Включення буферизації виводу
-   [ob\_get\_contents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [ob\_get\_flush()](function.ob-get-flush.html) - Скинути буфер виведення, повернути його у вигляді рядка та вимкнути буферизацію виводу
-   [ob\_flush()](function.ob-flush.html) - Скинути (надіслати) буфер виводу
-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу