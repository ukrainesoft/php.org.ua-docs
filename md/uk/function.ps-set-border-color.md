Встановлює колір межі анотацій

-   [«psscale](function.ps-scale.html)
    
-   [псsetborderdash »](function.ps-set-border-dash.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Встановлює колір межі анотацій
    

# псsetbordercolor

(PECL ps >= 1.1.0)

псsetbordercolor — Встановлює колір межі анотацій.

### Опис

```methodsynopsis
ps_set_border_color(    resource $psdoc,    float $red,    float $green,    float $blue): bool
```

Посилання, додані за допомогою однієї з функцій [псaddweblink()](function.ps-add-weblink.html) [псaddpdflink()](function.ps-add-pdflink.html) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює колір межі прямокутника.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`red`

Червоний компонент кольору кордону.

`green`

Зелений компонент кольору кордону.

`blue`

Синій компонент кольору кордону.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetborderdash()](function.ps-set-border-dash.html) - Встановлює довжину тире для межі анотації
-   [псsetborderstyle()](function.ps-set-border-style.html) - Встановлює стиль межі анотацій