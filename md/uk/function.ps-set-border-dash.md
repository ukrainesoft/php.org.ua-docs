---
navigation:
  - function.ps-set-border-color.md: «pssetbordercolor
  - function.ps-set-border-style.md: псsetborderstyle »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetborderdash
---
# псsetborderdash

(PECL ps >= 1.1.0)

псsetborderdash - Встановлює довжину тире для межі анотації.

### Опис

```methodsynopsis
ps_set_border_dash(resource $psdoc, float $black, float $white): bool
```

Посилання, додані за допомогою однієї з функцій [псaddweblink()](function.ps-add-weblink.md) [псaddpdflink()](function.ps-add-pdflink.md) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює зовнішній вигляд та ширину лінії кордону.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`black`

Довжина рисочки.

`white`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetbordercolor()](function.ps-set-border-color.md) - Встановлює колір межі анотацій
-   [псsetborderstyle()](function.ps-set-border-style.md) - Встановлює стиль межі анотацій
