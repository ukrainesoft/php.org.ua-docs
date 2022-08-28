Додати точку переривання на конкретний рядок файлу

-   [« Функции phpdbg](ref.phpdbg.html)
    
-   [phpdbg\_break\_function »](function.phpdbg-break-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции phpdbg](ref.phpdbg.html)
    
-   Додати точку переривання на конкретний рядок файлу
    

# phpdbgbreakfile

(PHP 5> = 5.6.3, PHP 7, PHP 8)

phpdbgbreakfile — Додати точку переривання на конкретний рядок файлу

### Опис

```methodsynopsis
phpdbg_break_file(string $file, int $line): void
```

Додає точку переривання на рядок `line` файлу `file`

### Список параметрів

`file`

Ім'я файлу.

`line`

Номер рядка.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_break\_function()](function.phpdbg-break-function.html) - Додати точку переривання на виклик функції
-   [phpdbg\_break\_method()](function.phpdbg-break-method.html) - Додати точку переривання на виклик методу класу
-   [phpdbg\_break\_next()](function.phpdbg-break-next.html) - Додати точку переривання на наступний опкод
-   [phpdbg\_clear()](function.phpdbg-clear.html) - Прибрати всі точки переривання