---
navigation:
  - function.ps-end-template.md: «psendtemplate
  - function.ps-fill.md: псfill »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псfillstroke
---
# псfillstroke

(PECL ps >= 1.1.0)

псfillstroke — Заповнює та обводить поточний шлях

### Опис

```methodsynopsis
ps_fill_stroke(resource $psdoc): bool
```

Заповнює та обводить шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [псlineto()](function.ps-lineto.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псfill()](function.ps-fill.md) - Заповнює поточний шлях
-   [псstroke()](function.ps-stroke.md) - Малює поточний шлях
