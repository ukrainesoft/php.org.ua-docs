---
navigation:
  - function.ps-save.md: « ps\_save
  - function.ps-set-border-color.md: ps\_set\_border\_color »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_scale
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_scale

(PECL ps >= 1.1.0)

ps\_scale — Встановлює коефіцієнт масштабування

### Опис

```methodsynopsis
ps_scale(resource $psdoc, float $x, float $y): bool
```

Встановлює горизонтальний та вертикальний масштаб системи координат.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`x`

Коефіцієнт масштабування горизонтальному напрямку.

`y`

Коефіцієнт масштабування за вертикаллю.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_rotate()](function.ps-rotate.md) \- Встановлює коефіцієнт обертання
-   [ps\_translate()](function.ps-translate.md) \- Змінює систему координат
