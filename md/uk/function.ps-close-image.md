---
navigation:
  - function.ps-clip.md: «psclip
  - function.ps-close.md: псclose »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псcloseimage
---
# псcloseimage

(PECL ps >= 1.1.0)

псcloseimage — Закриває зображення та звільняє пам'ять

### Опис

```methodsynopsis
ps_close_image(resource $psdoc, int $imageid): void|false
```

Закриває зображення та звільняє його ресурси. Як тільки зображення було закрито, його не можна використовувати.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`imageid`

Ідентифікатор ресурсу зображення, повернутий функцією [псopenimage()](function.ps-open-image.md) або [псopenimagefile()](function.ps-open-image-file.md)

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псopenimage()](function.ps-open-image.md) - Зчитує зображення для подальшого розміщення
-   [псopenimagefile()](function.ps-open-image-file.md) - Відкриває зображення із файлу
