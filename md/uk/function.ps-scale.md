Встановлює коефіцієнт масштабування

-   [«pssave](function.ps-save.html)
    
-   [псsetbordercolor »](function.ps-set-border-color.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює коефіцієнт масштабування
    

# псscale

(PECL ps >= 1.1.0)

псscale — Встановлює коефіцієнт масштабування

### Опис

```methodsynopsis
ps_scale(resource $psdoc, float $x, float $y): bool
```

Встановлює горизонтальний та вертикальний масштаб системи координат.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`x`

Коефіцієнт масштабування горизонтальному напрямку.

`y`

Коефіцієнт масштабування за вертикаллю.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псrotate()](function.ps-rotate.html) - Встановлює коефіцієнт обертання
-   [псtranslate()](function.ps-translate.html) - Змінює систему координат