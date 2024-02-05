---
navigation:
  - function.ps-end-template.md: « ps\_end\_template
  - function.ps-fill.md: ps\_fill »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_fill\_stroke
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_fill\_stroke

(PECL ps >= 1.1.0)

ps\_fill\_stroke — Заповнює та обводить поточний шлях

### Опис

```methodsynopsis
ps_fill_stroke(resource $psdoc): bool
```

Заповнює та обводить шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_fill()](function.ps-fill.md) \- Заповнює поточний шлях
-   [ps\_stroke()](function.ps-stroke.md) \- Малює поточний шлях
