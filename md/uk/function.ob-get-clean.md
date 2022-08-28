Отримати вміст поточного буфера та видалити його

-   [« ob\_flush](function.ob-flush.html)
    
-   [ob\_get\_contents »](function.ob-get-contents.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Отримати вміст поточного буфера та видалити його
    

# проgetclean

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

проgetclean — Отримати вміст поточного буфера та видалити його.

### Опис

```methodsynopsis
ob_get_clean(): string|false
```

Отримує вміст поточного буфера, а потім видаляє поточний буфер.

**проgetclean()** по суті виконує [ob\_get\_contents()](function.ob-get-contents.html) і [ob\_end\_clean()](function.ob-end-clean.html)

Буфер виводу має запускатися функцією [ob\_start()](function.ob-start.html) з прапорами [PHP\_OUTPUT\_HANDLER\_CLEANABLE](outcontrol.constants.html#constant.php-output-handler-cleanable) і [PHP\_OUTPUT\_HANDLER\_REMOVABLE](outcontrol.constants.html#constant.php-output-handler-removable). Інакше **проgetclean()** не спрацює.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст буфера виводу та закінчує буферизацію виводу. Якщо буферизація виводу не активована, то функція поверне **`false`**

### Приклади

**Приклад #1 Простий приклад використання функції **проgetclean()****

```php
<?php

ob_start();

echo "Привет мир";

$out = ob_get_clean();
$out = strtolower($out);

var_dump($out);
?>
```

Результат виконання цього прикладу:

```
string(11) "привет мир"
```

### Дивіться також

-   [ob\_get\_contents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [ob\_start()](function.ob-start.html) - Включення буферизації виводу