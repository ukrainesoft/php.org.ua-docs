---
navigation:
  - function.ps-rotate.html: «psrotate
  - function.ps-scale.html: псscale »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsave
---
# псsave

(PECL ps >= 1.1.0)

псsave — Зберігає поточний контекст

### Опис

```methodsynopsis
ps_save(resource $psdoc): bool
```

Зберігає поточний графічний контекст, що містить кольори, налаштування переміщення, повороту та багато іншого. Збережений контекст можна відновити за допомогою [псrestore()](function.ps-restore.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псrestore()](function.ps-restore.md) - Відновлює раніше збережений контекст
