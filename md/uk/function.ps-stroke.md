---
navigation:
  - function.ps-stringwidth.md: « ps\_stringwidth
  - function.ps-symbol-name.md: ps\_symbol\_name »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_stroke
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_stroke

(PECL ps >= 1.1.0)

ps\_stroke — Малює поточний шлях

### Опис

```methodsynopsis
ps_stroke(resource $psdoc): bool
```

Малює шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_closepath\_stroke()](function.ps-closepath-stroke.md) \- Замикає та обводить контур
-   [ps\_fill()](function.ps-fill.md) \- Заповнює поточний шлях
-   [ps\_fill\_stroke()](function.ps-fill-stroke.md) \- Заповнює та обводить поточний шлях
