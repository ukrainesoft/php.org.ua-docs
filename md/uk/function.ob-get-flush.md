Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу

-   [« ob\_get\_contents](function.ob-get-contents.html)
    
-   [ob\_get\_length »](function.ob-get-length.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу
    

# проgetflush

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проgetflush — Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу

### Опис

```methodsynopsis
ob_get_flush(): string|false
```

**проgetflush()** скидає буфер виведення, повертаючи його вміст у вигляді рядка та відключає буферизацію виведення.

Буфер виводу має запускатися функцією [ob\_start()](function.ob-start.html) з прапором [PHP\_OUTPUT\_HANDLER\_FLUSHABLE](outcontrol.constants.html#constant.php-output-handler-flushable). Інакше не спрацює **проgetflush()**

> **Зауваження**: Ця функція аналогічна [ob\_end\_flush()](function.ob-end-flush.html) крім того, що ця функція також повертає буфер у вигляді рядка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає буфер виводу або **`false`**якщо буферизація не активна.

### Приклади

**Приклад #1 Приклад використання функції **проgetflush()****

```php
<?php
//Используется output_buffering=On
print_r(ob_list_handlers());

//сохранить буфер в файл
$buffer = ob_get_flush();
file_put_contents('buffer.txt', $buffer);

print_r(ob_list_handlers());
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
)
```

### Дивіться також

-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
-   [ob\_end\_flush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [ob\_list\_handlers()](function.ob-list-handlers.html) - Список всіх використовуваних обробників виводу