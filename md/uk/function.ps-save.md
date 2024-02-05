---
navigation:
  - function.ps-rotate.md: « ps\_rotate
  - function.ps-scale.md: ps\_scale »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_save
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_save

(PECL ps >= 1.1.0)

ps\_save — Зберігає поточний контекст

### Опис

```methodsynopsis
ps_save(resource $psdoc): bool
```

Зберігає поточний графічний контекст, що містить кольори, налаштування переміщення, повороту та багато іншого. Збережений контекст можна відновити за допомогою [ps\_restore()](function.ps-restore.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_restore()](function.ps-restore.md) \- Відновлює раніше збережений контекст
