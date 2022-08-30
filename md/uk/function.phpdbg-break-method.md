Додати точку переривання на виклик методу класу

-   [« phpdbgbreakfunction](function.phpdbg-break-function.html)
    
-   [phpdbgbreaknext »](function.phpdbg-break-next.html)
    
-   [PHP Manual](index.md)
    
-   [Функции phpdbg](ref.phpdbg.md)
    
-   Додати точку переривання на виклик методу класу
    

# phpdbgbreakметод

(PHP 5> = 5.6.3, PHP 7, PHP 8)

phpdbgbreakmethod — Додати точку переривання на виклик методу класу

### Опис

```methodsynopsis
phpdbg_break_method(string $class, string $method): void
```

Додає точку переривання на виклик методу `method` класу `class`

### Список параметрів

`class`

Назва класу.

`method`

Ім'я методу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgbreakfile()](function.phpdbg-break-file.html) - Додати точку переривання на конкретний рядок файлу
-   [phpdbgbreakfunction()](function.phpdbg-break-function.html) - Додати точку переривання на виклик функції
-   [phpdbgbreaknext()](function.phpdbg-break-next.html) - Додати точку переривання на наступний опкод
-   [phpdbgclear()](function.phpdbg-clear.html) - Прибрати всі точки переривання