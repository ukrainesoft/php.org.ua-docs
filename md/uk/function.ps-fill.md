---
navigation:
  - function.ps-fill-stroke.md: « ps\_fill\_stroke
  - function.ps-findfont.md: ps\_findfont »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_fill
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_fill

(PECL ps >= 1.1.0)

ps\_fill — Заповнює поточний шлях

### Опис

```methodsynopsis
ps_fill(resource $psdoc): bool
```

Заповнює шлях, створений за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_fill\_stroke()](function.ps-fill-stroke.md) \- Заповнює та обводить поточний шлях
-   [ps\_stroke()](function.ps-stroke.md) \- Малює поточний шлях
