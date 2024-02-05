---
navigation:
  - function.ps-set-border-color.md: « ps\_set\_border\_color
  - function.ps-set-border-style.md: ps\_set\_border\_style »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_border\_dash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_border\_dash

(PECL ps >= 1.1.0)

ps\_set\_border\_dash - Встановлює довжину тире для межі анотації.

### Опис

```methodsynopsis
ps_set_border_dash(resource $psdoc, float $black, float $white): bool
```

Посилання, додані однією з функцій [ps\_add\_weblink()](function.ps-add-weblink.md) [ps\_add\_pdflink()](function.ps-add-pdflink.md) і т. д., будуть відображатися із закругленим прямокутником, коли документ PostScript перетворюється на PDF і переглядається у програмі перегляду PDF. Цей прямокутник не відображається у документі PostScript. Функція встановлює зовнішній вигляд та ширину лінії кордону.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`black`

Довжина рисочки.

`white`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_set\_border\_color()](function.ps-set-border-color.md) \- Встановлює колір межі анотацій
-   [ps\_set\_border\_style()](function.ps-set-border-style.md) \- Встановлює стиль межі анотацій
