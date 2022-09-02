---
navigation:
  - function.ps-stringwidth.md: «psstringwidth
  - function.ps-symbol-name.md: псsymbolname »
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

Малює шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [псlineto()](function.ps-lineto.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclosepathstroke()](function.ps-closepath-stroke.md) - Замикає та обводить контур
-   [псfill()](function.ps-fill.md) - Заповнює поточний шлях
-   [псfillstroke()](function.ps-fill-stroke.md) - Заповнює та обводить поточний шлях
