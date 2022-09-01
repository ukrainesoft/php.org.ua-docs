---
navigation:
  - function.ps-rect.html: «psrect
  - function.ps-rotate.html: псrotate »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псrestore
---
# псrestore

(PECL ps >= 1.1.0)

псrestore — Відновлює раніше збережений контекст

### Опис

```methodsynopsis
ps_restore(resource $psdoc): bool
```

Відновлює раніше збережений графічний контекст. Будь-який виклик [псsave()](function.ps-save.html) повинен супроводжуватись викликом **псrestore()**. Усі перетворення координат, налаштування стилю ліній, налаштування кольору тощо. відновлюються до стану до дзвінка [псsave()](function.ps-save.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsave()](function.ps-save.html) - Зберігає поточний контекст
