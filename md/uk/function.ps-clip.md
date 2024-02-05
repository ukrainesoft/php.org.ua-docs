---
navigation:
  - function.ps-circle.md: « ps\_circle
  - function.ps-close-image.md: ps\_close\_image »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_clip
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_clip

(PECL ps >= 1.1.0)

ps\_clip — Відтворення кліпів поточним шляхом

### Опис

```methodsynopsis
ps_clip(resource $psdoc): bool
```

Бере поточний шлях та використовує його для визначення межі області відсікання. Все, що намальовано за межами цієї галузі, не буде видно.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_closepath()](function.ps-closepath.md) \- Замикає шлях
