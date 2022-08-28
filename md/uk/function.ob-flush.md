Скинути (надіслати) буфер виводу

-   [« ob\_end\_flush](function.ob-end-flush.html)
    
-   [ob\_get\_clean »](function.ob-get-clean.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Скинути (надіслати) буфер виводу
    

# проflush

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проflush — Скинути (надіслати) буфер виводу

### Опис

```methodsynopsis
ob_flush(): bool
```

Ця функція надішле вміст буфера виводу (якщо є). Якщо необхідна подальша обробка буфера виводу, слід викликати [ob\_get\_contents()](function.ob-get-contents.html) перед **проflush()**, оскільки вміст буфера буде видалено після виклику **проflush()**

Ця функція не знищує буфер виводу, як це робить [ob\_end\_flush()](function.ob-end-flush.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ob\_get\_contents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [ob\_clean()](function.ob-clean.html) - Очистити (стерти) буфер виводу
-   [ob\_end\_flush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу