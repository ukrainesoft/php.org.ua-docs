Список всіх обробників виводу, що використовуються

-   [« ob\_implicit\_flush](function.ob-implicit-flush.html)
    
-   [ob\_start »](function.ob-start.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Список всіх обробників виводу, що використовуються
    

# проlisthandlers

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проlisthandlers — Список всіх обробників виводу, що використовуються.

### Опис

```methodsynopsis
ob_list_handlers(): array
```

Список всіх обробників виведення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція поверне масив із використовуваними обробниками виводу (якщо є). Якщо увімкнено [output\_buffering](outcontrol.configuration.html#ini.output-buffering) або використовувалася анонімна функція разом з [ob\_start()](function.ob-start.html), то **проlisthandlers()** поверне "default output handler".

### Приклади

**Приклад #1 Приклад використання функції **проlisthandlers()****

```php
<?php
//используется output_buffering=On
print_r(ob_list_handlers());
ob_end_flush();

ob_start("ob_gzhandler");
print_r(ob_list_handlers());
ob_end_flush();

// анонимная функция
ob_start(function($string) { return $string; });
print_r(ob_list_handlers());
ob_end_flush();
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => default output handler
)

Array
(
    [0] => ob_gzhandler
)

Array
(
    [0] => Closure::__invoke
)
```

### Дивіться також

-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
-   [ob\_end\_flush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [ob\_get\_flush()](function.ob-get-flush.html) - Скинути буфер виведення, повернути його у вигляді рядка та вимкнути буферизацію виводу
-   [ob\_start()](function.ob-start.html) - Включення буферизації виводу