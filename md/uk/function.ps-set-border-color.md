---
navigation:
  - function.ps-scale.md: « ps\_scale
  - function.ps-set-border-dash.md: ps\_set\_border\_dash »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_border\_color
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_border\_color

(PECL ps >= 1.1.0)

ps\_set\_border\_color — Встановлює колір межі анотацій.

### Опис

```methodsynopsis
ps_set_border_color(    resource $psdoc,    float $red,    float $green,    float $blue): bool
```

Посилання, додані однією з функцій [ps\_add\_weblink()](function.ps-add-weblink.md) [ps\_add\_pdflink()](function.ps-add-pdflink.md) і т. д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює колір межі прямокутника.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`red`

Червоний компонент кольору кордону.

`green`

Зелений компонент кольору кордону.

`blue`

Синій компонент кольору кордону.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_set\_border\_dash()](function.ps-set-border-dash.md) \- Встановлює довжину тире для межі анотації
-   [ps\_set\_border\_style()](function.ps-set-border-style.md) \- Встановлює стиль межі анотацій
