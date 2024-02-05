---
navigation:
  - function.ps-rect.md: « ps\_rect
  - function.ps-rotate.md: ps\_rotate »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_restore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_restore

(PECL ps >= 1.1.0)

ps\_restore — Відновлює раніше збережений контекст

### Опис

```methodsynopsis
ps_restore(resource $psdoc): bool
```

Відновлює раніше збережений графічний контекст. Будь-який виклик [ps\_save()](function.ps-save.md) повинен супроводжуватись викликом **ps\_restore()**. Усі перетворення координат, налаштування стилю ліній, налаштування кольору тощо. відновлюються до стану до дзвінка [ps\_save()](function.ps-save.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_save()](function.ps-save.md) \- Зберігає поточний контекст
