Встановлює шрифт, який використовуватиметься для наступного висновку

-   [« ps\_setflat](function.ps-setflat.html)
    
-   [ps\_setgray »](function.ps-setgray.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює шрифт, який використовуватиметься для наступного висновку
    

# пссетфонт

(PECL ps >= 1.1.0)

псsetfont — Встановлює шрифт, який буде використовуватись для наступного виводу

### Опис

```methodsynopsis
ps_setfont(resource $psdoc, int $fontid, float $size): bool
```

Встановлює шрифт, який має бути завантажений раніше за допомогою [ps\_findfont()](function.ps-findfont.html). Виведення тексту без встановлення шрифту призводить до помилки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`fontid`

Ідентифікатор шрифту, повернутий [ps\_findfont()](function.ps-findfont.html)

`size`

Розмір шрифту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_findfont()](function.ps-findfont.html) - Завантажує шрифт
-   [ps\_set\_text\_pos()](function.ps-set-text-pos.html) - Встановлює позицію для виведення тексту на приклад.