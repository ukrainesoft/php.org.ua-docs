Отримує геометрію рядка

-   [«psshow](function.ps-show.html)
    
-   [псstringwidth »](function.ps-stringwidth.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Отримує геометрію рядка
    

# псstringgeometry

(PECL ps >= 1.2.0)

псstringgeometry — Отримує геометрію рядка

### Опис

```methodsynopsis
ps_string_geometry(    resource $psdoc,    string $text,    int $fontid = 0,    float $size = 0.0): array
```

Функція схожа на [псstringwidth()](function.ps-stringwidth.html), але повертає масив розмірів, що містить ширину, верхню та нижню межу тексту.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`text`

Текст, для якого має бути розрахована геометрія.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовується поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Масив розмірів рядка. Елемент "width" містить ширину рядка, що повертається функцією [псstringwidth()](function.ps-stringwidth.html). Елемент "descender" містить максимальну нижню межу, а "ascender" - максимальну верхню межу елемента рядка.

### Дивіться також

-   [псcontinuetext()](function.ps-continue-text.html) - Продовжує текст у наступному рядку
-   [псstringwidth()](function.ps-stringwidth.html) - Отримує ширину рядка