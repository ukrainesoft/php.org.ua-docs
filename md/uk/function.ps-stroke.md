---
navigation:
  - function.ps-stringwidth.html: «psstringwidth
  - function.ps-symbol-name.html: псsymbolname »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псstroke
---
# псstroke

(PECL ps >= 1.1.0)

псstroke — Малює поточний шлях

### Опис

```methodsynopsis
ps_stroke(resource $psdoc): bool
```

Малює шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [псlineto()](function.ps-lineto.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclosepathstroke()](function.ps-closepath-stroke.html) - Замикає та обводить контур
-   [псfill()](function.ps-fill.html) - Заповнює поточний шлях
-   [псfillstroke()](function.ps-fill-stroke.html) - Заповнює та обводить поточний шлях
