---
navigation:
  - function.ps-close.md: « ps\_close
  - function.ps-closepath.md: ps\_closepath »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_closepath\_stroke
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_closepath\_stroke

(PECL ps >= 1.1.0)

ps\_closepath\_stroke — Замикає та обводить контур

### Опис

```methodsynopsis
ps_closepath_stroke(resource $psdoc): bool
```

З'єднує останню точку з першою точкою шляху і малює замкнуту лінію, що вийшла.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_closepath()](function.ps-closepath.md) \- Замикає шлях
