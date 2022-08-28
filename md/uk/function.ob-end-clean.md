Очистити (стерти) буфер виводу та вимкнути буферизацію виводу

-   [« ob\_clean](function.ob-clean.html)
    
-   [ob\_end\_flush »](function.ob-end-flush.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
    

# проendclean

(PHP 4, PHP 5, PHP 7, PHP 8)

проendclean — Очистити (стерти) буфер виводу та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_end_clean(): bool
```

Ця функція видаляє вміст верхнього буфера виводу і відключає цю буферизацію. Якщо ви хочете використати вміст буфера, то вам необхідно викликати [ob\_get\_contents()](function.ob-get-contents.html) перед **проendclean()**, оскільки весь вміст буфера видаляється при виклику **проendclean()**

Буфер виводу має запускатися функцією [ob\_start()](function.ob-start.html) з прапорами [PHP\_OUTPUT\_HANDLER\_CLEANABLE](outcontrol.constants.html#constant.php-output-handler-cleanable) і [PHP\_OUTPUT\_HANDLER\_REMOVABLE](outcontrol.constants.html#constant.php-output-handler-removable). Інакше не спрацює **проendclean()**

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

-   [ob\_start()](function.ob-start.html) - Включення буферизації виводу
-   [ob\_get\_contents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [ob\_flush()](function.ob-flush.html) - Скинути (надіслати) буфер виводу