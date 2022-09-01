---
navigation:
  - imagick.tintimage.html: '« Imagick::tintImage'
  - imagick.transformimage.html: 'Imagick::transformImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::toString'
---
# Imagick::toString

(PECL imagick 2, PECL imagick 3)

Imagick::toString — Повертає зображення у вигляді рядка

### Опис

```methodsynopsis
public Imagick::__toString(): string
```

Повертає поточне зображення у вигляді рядка. Поверне лише одне зображення; Метод не повинен використовуватися для об'єктів Imagick, які містять кілька зображень, наприклад, анімований GIF або PDF з кількома сторінками.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст рядка у разі успішного виконання або порожній рядок у разі помилки.

### Дивіться також

-   [Imagick::getImageBlob()](imagick.getimageblob.html) - Повертає послідовність зображень у вигляді BLOB
-   [Imagick::getImagesBlob()](imagick.getimagesblob.html) - Повертає всі послідовності зображень у вигляді великого двійкового об'єкта
