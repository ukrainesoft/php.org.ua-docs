---
navigation:
  - function.ps-clip.md: « ps\_clip
  - function.ps-close.md: ps\_close »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_close\_image
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_close\_image

(PECL ps >= 1.1.0)

ps\_close\_image — Закриває зображення та звільняє пам'ять

### Опис

```methodsynopsis
ps_close_image(resource $psdoc, int $imageid): void|false
```

Закриває зображення та звільняє його ресурси. Як тільки зображення було закрито, його не можна використовувати.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`imageid`

Ідентифікатор ресурсу зображення, повернутий функцією [ps\_open\_image()](function.ps-open-image.md) або [ps\_open\_image\_file()](function.ps-open-image-file.md)

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_open\_image()](function.ps-open-image.md) \- Зчитує зображення для подальшого розміщення
-   [ps\_open\_image\_file()](function.ps-open-image-file.md) \- Відкриває зображення із файлу
