Сінус

-   [« round](function.round.html)
    
-   [sinh »](function.sinh.html)
    
-   [PHP Manual](index.html)
    
-   [Математичні функції](ref.math.html)
    
-   Сінус
    

# sin

(PHP 4, PHP 5, PHP 7, PHP 8)

sin - Сінус

### Опис

```methodsynopsis
sin(float $num): float
```

**sin()** повертає синус параметра `num`. Параметр `num` задається у радіанах.

### Список параметрів

`num`

Значення у радіанах

### Значення, що повертаються

Синус кута `num`

### Приклади

**Приклад #1 Приклад використання **sin()****

```php
<?php

// Точность зависит от ваших настроек точности
echo sin(deg2rad(60));  //  0.866025403 ...
echo sin(60);           // -0.304810621 ...

?>
```

### Дивіться також

-   [asin()](function.asin.html) - Арксінус
-   [sinh()](function.sinh.html) - Гіперболічний синус
-   [cos()](function.cos.html) - Косінус
-   [tan()](function.tan.html) - Тангенс
-   [deg2rad()](function.deg2rad.html) - Перетворює значення із градусів на радіани