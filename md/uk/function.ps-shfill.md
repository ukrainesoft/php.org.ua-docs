Заповнює область затіненням

-   [«psshading](function.ps-shading.html)
    
-   [псshowboxed »](function.ps-show-boxed.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Заповнює область затіненням
    

# псshfill

(PECL ps >= 1.3.0)

псshfill - Заповнює область затіненням

### Опис

```methodsynopsis
ps_shfill(resource $psdoc, int $shadingid): bool
```

Заповнює область затіненням, яке має бути створене раніше за допомогою [псshading()](function.ps-shading.html). Це альтернативний спосіб створення візерунка із затінення [псshadingpattern()](function.ps-shading-pattern.html) і використання візерунка як колір заливки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`shadingid`

Ідентифікатор затінення, створеного раніше за допомогою [псshading()](function.ps-shading.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псshading()](function.ps-shading.html) - Створює затінення для подальшого використання
-   [псshadingpattern()](function.ps-shading-pattern.html) - Створює візерунок на основі затінення