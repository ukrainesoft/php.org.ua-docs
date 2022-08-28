Очистити (стерти) буфер виводу

-   [« flush](function.flush.html)
    
-   [ob\_end\_clean »](function.ob-end-clean.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Очистити (стерти) буфер виводу
    

# проclean

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проclean — Очистити (стерти) буфер виводу

### Опис

```methodsynopsis
ob_clean(): bool
```

Ця функція очищає вміст вихідного буфера, не надсилаючи його до браузера.

Ця функція не знищує буфер виводу, як це робить [ob\_end\_clean()](function.ob-end-clean.html)

Буфер виводу має запускатися функцією [ob\_start()](function.ob-start.html) з прапором [PHP\_OUTPUT\_HANDLER\_CLEANABLE](outcontrol.constants.html#constant.php-output-handler-cleanable). Інакше **проclean()** не спрацює.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ob\_flush()](function.ob-flush.html) - Скинути (надіслати) буфер виводу
-   [ob\_end\_flush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виводу та вимкнути буферизацію виводу