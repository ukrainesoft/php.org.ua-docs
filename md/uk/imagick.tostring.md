---
navigation:
  - imagick.tintimage.md: '« Imagick::tintImage'
  - imagick.transformimage.md: 'Imagick::transformImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::\_\_function toString() { \[native code\] }

(PECL imagick 2, PECL imagick 3)

Imagick::\_\_toString — Повертає зображення у вигляді рядка

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

-   [Imagick::getImageBlob()](imagick.getimageblob.md) \- Повертає послідовність зображень у вигляді BLOB
-   [Imagick::getImagesBlob()](imagick.getimagesblob.md) \- Повертає всі послідовності зображень у вигляді великого двійкового об'єкта
