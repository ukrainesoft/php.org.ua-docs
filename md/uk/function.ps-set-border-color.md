Встановлює колір межі анотацій

-   [« ps\_scale](function.ps-scale.html)
    
-   [ps\_set\_border\_dash »](function.ps-set-border-dash.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює колір межі анотацій
    

# псsetbordercolor

(PECL ps >= 1.1.0)

псsetbordercolor — Встановлює колір межі анотацій.

### Опис

```methodsynopsis
ps_set_border_color(    resource $psdoc,    float $red,    float $green,    float $blue): bool
```

Посилання, додані за допомогою однієї з функцій [ps\_add\_weblink()](function.ps-add-weblink.html) [ps\_add\_pdflink()](function.ps-add-pdflink.html) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює колір межі прямокутника.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`red`

Червоний компонент кольору кордону.

`green`

Зелений компонент кольору кордону.

`blue`

Синій компонент кольору кордону.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_set\_border\_dash()](function.ps-set-border-dash.html) - Встановлює довжину тире для межі анотації
-   [ps\_set\_border\_style()](function.ps-set-border-style.html) - Встановлює стиль межі анотацій