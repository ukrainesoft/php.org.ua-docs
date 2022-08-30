Встановлює шрифт, який використовуватиметься для наступного висновку

-   [«pssetflat](function.ps-setflat.html)
    
-   [псsetgray »](function.ps-setgray.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює шрифт, який використовуватиметься для наступного висновку
    

# пссетфонт

(PECL ps >= 1.1.0)

псsetfont — Встановлює шрифт, який буде використовуватись для наступного виводу

### Опис

```methodsynopsis
ps_setfont(resource $psdoc, int $fontid, float $size): bool
```

Встановлює шрифт, який має бути завантажений раніше за допомогою [псfindfont()](function.ps-findfont.html). Виведення тексту без встановлення шрифту призводить до помилки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`fontid`

Ідентифікатор шрифту, повернутий [псfindfont()](function.ps-findfont.html)

`size`

Розмір шрифту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псfindfont()](function.ps-findfont.html) - Завантажує шрифт
-   [псsettextpos()](function.ps-set-text-pos.html) - Встановлює позицію для виведення тексту на приклад.