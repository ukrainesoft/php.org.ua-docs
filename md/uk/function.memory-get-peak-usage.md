Повертає пікове значення об'єму пам'яті, виділене PHP

-   [« ini\_set](function.ini-set.html)
    
-   [memory\_get\_usage »](function.memory-get-usage.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Повертає пікове значення об'єму пам'яті, виділене PHP
    

# memorygetpeakusage

(PHP 5> = 5.2.0, PHP 7, PHP 8)

memorygetpeakusage — Повертає пікове значення об'єму пам'яті, виділене PHP

### Опис

```methodsynopsis
memory_get_peak_usage(bool $real_usage = false): int
```

Повертає максимальний обсяг пам'яті в байтах, виділений PHP-скрипту.

### Список параметрів

`real_usage`

Передача **`true`** як цей аргумент дозволяє отримати реальний обсяг пам'яті, виділений системою. Якщо аргумент не заданий чи дорівнює **`false`**, повертаються відомості лише про пам'ять, виділену функцією `emalloc()`

### Значення, що повертаються

Повертає максимальний обсяг пам'яті у байтах.

### Дивіться також

-   [memory\_get\_usage()](function.memory-get-usage.html) - Повертає кількість пам'яті, виділену для PHP
-   [memory\_limit](ini.core.html#ini.memory-limit)