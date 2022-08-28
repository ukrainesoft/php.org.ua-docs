Встановлює коефіцієнт масштабування

-   [« ps\_save](function.ps-save.html)
    
-   [ps\_set\_border\_color »](function.ps-set-border-color.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`x`

Коефіцієнт масштабування горизонтальному напрямку.

`y`

Коефіцієнт масштабування за вертикаллю.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_rotate()](function.ps-rotate.html) - Встановлює коефіцієнт обертання
-   [ps\_translate()](function.ps-translate.html) - Змінює систему координат