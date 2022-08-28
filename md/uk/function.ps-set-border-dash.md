Встановлює довжину тире для межі анотації

-   [« ps\_set\_border\_color](function.ps-set-border-color.html)
    
-   [ps\_set\_border\_style »](function.ps-set-border-style.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює довжину тире для межі анотації
    

# псsetborderdash

(PECL ps >= 1.1.0)

псsetborderdash - Встановлює довжину тире для межі анотації.

### Опис

```methodsynopsis
ps_set_border_dash(resource $psdoc, float $black, float $white): bool
```

Посилання, додані за допомогою однієї з функцій [ps\_add\_weblink()](function.ps-add-weblink.html) [ps\_add\_pdflink()](function.ps-add-pdflink.html) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює зовнішній вигляд та ширину лінії кордону.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`black`

Довжина рисочки.

`white`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_set\_border\_color()](function.ps-set-border-color.html) - Встановлює колір межі анотацій
-   [ps\_set\_border\_style()](function.ps-set-border-style.html) - Встановлює стиль межі анотацій