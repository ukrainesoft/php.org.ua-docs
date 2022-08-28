Створює візерунок на основі затінення

-   [« ps\_setpolydash](function.ps-setpolydash.html)
    
-   [ps\_shading »](function.ps-shading.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Створює візерунок на основі затінення
    

# псshadingpattern

(PECL ps >= 1.3.0)

псshadingpattern — Створює візерунок на основі затінення

### Опис

```methodsynopsis
ps_shading_pattern(resource $psdoc, int $shadingid, string $optlist): int|false
```

Створює візерунок на основі затінення, яке має бути створене раніше за допомогою [ps\_shading()](function.ps-shading.html). Затінення шаблони можна використовувати як звичайні шаблони.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`shadingid`

Ідентифікатор затінення, створеного раніше за допомогою [ps\_shading()](function.ps-shading.html)

`optlist`

Аргумент нині не використовується.

### Значення, що повертаються

Ідентифікатор шаблону або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_shading()](function.ps-shading.html) - Створює затінення для подальшого використання
-   [ps\_shfill()](function.ps-shfill.html) - Заповнює область затіненням