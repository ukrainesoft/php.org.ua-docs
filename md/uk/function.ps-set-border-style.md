Встановлює стиль межі анотацій

-   [« ps\_set\_border\_dash](function.ps-set-border-dash.html)
    
-   [ps\_set\_info »](function.ps-set-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює стиль межі анотацій
    

# псsetborderstyle

(PECL ps >= 1.1.0)

псsetborderstyle — Встановлює стиль межі анотацій

### Опис

```methodsynopsis
ps_set_border_style(resource $psdoc, string $style, float $width): bool
```

Посилання, додані за допомогою однієї з функцій [ps\_add\_weblink()](function.ps-add-weblink.html) [ps\_add\_pdflink()](function.ps-add-pdflink.html) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює зовнішній вигляд та ширину лінії кордону.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`style`

`style` може бути `solid` або `dashed`

`width`

Ширина лінії кордону.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_set\_border\_color()](function.ps-set-border-color.html) - Встановлює колір межі анотацій
-   [ps\_set\_border\_dash()](function.ps-set-border-dash.html) - Встановлює довжину тире для межі анотації