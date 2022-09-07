---
navigation:
  - function.ps-setfont.md: «pssetfont
  - function.ps-setlinecap.md: псsetlinecap »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
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

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`gray`

Значення повинне бути від 0 (білий) до 1 (чорний).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetcolor()](function.ps-setcolor.md) - Встановлює поточний колір
