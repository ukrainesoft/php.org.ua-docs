---
navigation:
  - function.ps-save.md: «pssave
  - function.ps-set-border-color.md: псsetbordercolor »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псscale
---
# псscale

(PECL ps >= 1.1.0)

псscale — Встановлює коефіцієнт масштабування

### Опис

```methodsynopsis
ps_scale(resource $psdoc, float $x, float $y): bool
```

Встановлює горизонтальний та вертикальний масштаб системи координат.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`x`

Коефіцієнт масштабування горизонтальному напрямку.

`y`

Коефіцієнт масштабування за вертикаллю.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псrotate()](function.ps-rotate.md) - Встановлює коефіцієнт обертання
-   [псtranslate()](function.ps-translate.md) - Змінює систему координат
