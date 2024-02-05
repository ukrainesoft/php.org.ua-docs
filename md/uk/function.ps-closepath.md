---
navigation:
  - function.ps-closepath-stroke.md: « ps\_closepath\_stroke
  - function.ps-continue-text.md: ps\_continue\_text »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_closepath
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_closepath

(PECL ps >= 1.1.0)

ps\_closepath - Замикає шлях

### Опис

```methodsynopsis
ps_closepath(resource $psdoc): bool
```

Поєднує останню точку з першою точкою шляху. Отриманий контур можна використовувати для обведення, заливки, обрізки тощо.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_clip()](function.ps-clip.md) \- Відображення кліпів по поточному шляху
-   [ps\_closepath\_stroke()](function.ps-closepath-stroke.md) \- Замикає та обводить контур
