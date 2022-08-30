Створює затінення для подальшого використання

-   [«psshadingpattern](function.ps-shading-pattern.html)
    
-   [псshfill »](function.ps-shfill.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Створює затінення для подальшого використання
    

# псshading

(PECL ps >= 1.3.0)

псshading — Створює затінення для подальшого використання

### Опис

```methodsynopsis
ps_shading(    resource $psdoc,    string $type,    float $x0,    float $y0,    float $x1,    float $y1,    float $c1,    float $c2,    float $c3,    float $c4,    string $optlist): int|false
```

Створює затінення, яке можна використовувати функцією [псshfill()](function.ps-shfill.html) або [псshadingpattern()](function.ps-shading-pattern.html)

Колір затінення може бути в будь-якому колірному просторі, крім `pattern`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`type`

Тип затінення може бути `radial` або `axial`. Кожне затінення починається з поточного кольору заливки та закінчується заданими значеннями кольору, переданими у параметрах від `c1` до `c4` (опис їх значень дивіться в [псsetcolor()](function.ps-setcolor.html)

`x0, x1, y0, y1`

Координати `x0` `y0` `x1` `y1` - це початкова та кінцева точки затінення. Якщо тип затінення - `radial`, дві точки є середніми точками початкового та кінцевого кіл.

`c1, c2, c3, c4`

Дивіться опис їх значень у [псsetcolor()](function.ps-setcolor.html)

`optlist`

Якщо тип затінення `radial` `optlist` також має містити параметри `r0` і `r1` з радіусом початкового та кінцевого кола.

### Значення, що повертаються

Повертає ідентифікатор шаблону або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псshadingpattern()](function.ps-shading-pattern.html) - Створює візерунок на основі затінення
-   [псshfill()](function.ps-shfill.html) - Заповнює область затіненням