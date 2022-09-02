---
navigation:
  - function.ps-circle.md: «pscircle
  - function.ps-close-image.md: псcloseimage »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псclip
---
# псclip

(PECL ps >= 1.1.0)

псclip — Відтворення кліпів поточним шляхом

### Опис

```methodsynopsis
ps_clip(resource $psdoc): bool
```

Бере поточний шлях та використовує його для визначення межі області відсікання. Все, що намальовано за межами цієї галузі, не буде видно.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclosepath()](function.ps-closepath.md) - Замикає шлях
