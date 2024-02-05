---
navigation:
  - function.ps-setfont.md: « ps\_setfont
  - function.ps-setlinecap.md: ps\_setlinecap »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setgray
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setgray

(PECL ps >= 1.1.0)

ps\_setgray - Встановлює значення сірого

### Опис

```methodsynopsis
ps_setgray(resource $psdoc, float $gray): bool
```

Встановлює значення сірого всіх наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`gray`

Значення повинне бути від 0 (білий) до 1 (чорний).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_setcolor()](function.ps-setcolor.md) \- Встановлює поточний колір
