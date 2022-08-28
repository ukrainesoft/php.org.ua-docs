Заповнює область затіненням

-   [« ps\_shading](function.ps-shading.html)
    
-   [ps\_show\_boxed »](function.ps-show-boxed.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Заповнює область затіненням
    

# псshfill

(PECL ps >= 1.3.0)

псshfill - Заповнює область затіненням

### Опис

```methodsynopsis
ps_shfill(resource $psdoc, int $shadingid): bool
```

Заповнює область затіненням, яке має бути створене раніше за допомогою [ps\_shading()](function.ps-shading.html). Це альтернативний спосіб створення візерунка із затінення [ps\_shading\_pattern()](function.ps-shading-pattern.html) і використання візерунка як колір заливки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`shadingid`

Ідентифікатор затінення, створеного раніше за допомогою [ps\_shading()](function.ps-shading.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_shading()](function.ps-shading.html) - Створює затінення для подальшого використання
-   [ps\_shading\_pattern()](function.ps-shading-pattern.html) - Створює візерунок на основі затінення