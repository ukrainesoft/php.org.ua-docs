---
navigation:
  - function.ps-set-border-dash.html: «pssetborderdash
  - function.ps-set-info.html: псsetinfo »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetborderstyle
---
# псsetborderstyle

(PECL ps >= 1.1.0)

псsetborderstyle — Встановлює стиль межі анотацій

### Опис

```methodsynopsis
ps_set_border_style(resource $psdoc, string $style, float $width): bool
```

Посилання, додані за допомогою однієї з функцій [псaddweblink()](function.ps-add-weblink.html) [псaddpdflink()](function.ps-add-pdflink.html) і т.д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює зовнішній вигляд та ширину лінії кордону.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`style`

`style` може бути `solid` або `dashed`

`width`

Ширина лінії кордону.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetbordercolor()](function.ps-set-border-color.html) - Встановлює колір межі анотацій
-   [псsetborderdash()](function.ps-set-border-dash.html) - Встановлює довжину тире для межі анотації
