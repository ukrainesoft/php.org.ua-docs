---
navigation:
  - function.ps-setfont.html: «pssetfont
  - function.ps-setlinecap.html: псsetlinecap »
  - index.html: PHP Manual
  - ref.ps.html: Функції PS
title: псsetgray
---
# псsetgray

(PECL ps >= 1.1.0)

псsetgray - Встановлює значення сірого

### Опис

```methodsynopsis
ps_setgray(resource $psdoc, float $gray): bool
```

Встановлює значення сірого всіх наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`gray`

Значення повинне бути від 0 (білий) до 1 (чорний).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetcolor()](function.ps-setcolor.html) - Встановлює поточний колір
