Задати колір елементу

-   [« phpdbg\_clear](function.phpdbg-clear.html)
    
-   [phpdbg\_end\_oplog »](function.phpdbg-end-oplog.html)
    
-   [PHP Manual](index.html)
    
-   [Функции phpdbg](ref.phpdbg.html)
    
-   Задати колір елементу
    

# phpdbgcolor

(PHP 5> = 5.6.0, PHP 7, PHP 8)

phpdbgcolor — Задати колір елементу

### Опис

```methodsynopsis
phpdbg_color(int $element, string $color): void
```

Встановлює колір `color` для елемента `element`

### Список параметрів

`element`

Одна з констант **`PHPDBG_COLOR_*`**

`color`

Назва кольору. Одне з: `white` `red` `green` `yellow` `blue` `purple` `cyan` або `black`. Опціонально можна використовувати суфікси `-bold` або `-underline`. Наприклад `white-bold` або `green-underline`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_prompt()](function.phpdbg-prompt.html) - встановити запрошення командного рядка