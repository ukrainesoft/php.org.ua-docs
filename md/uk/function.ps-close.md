---
navigation:
  - function.ps-close-image.md: «pscloseimage
  - function.ps-closepath-stroke.md: псclosepathstroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псclose
---
# псclose

(PECL ps >= 1.1.0)

псclose — Закриває документ PostScript

### Опис

```methodsynopsis
ps_close(resource $psdoc): bool
```

Закриває документ PostScript.

Функція записує кількість сторінок у документі PostScript. Вона також записує ієрархію закладок . **псclose()** не звільняє ресурси, як [псdelete()](function.ps-delete.md)

Функція також викликається функцією [псdelete()](function.ps-delete.md)якщо вона не була викликана раніше.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псopenfile()](function.ps-open-file.md) - Відкриває файл для виводу
-   [псdelete()](function.ps-delete.md) - Видаляє всі ресурси документа PostScript
