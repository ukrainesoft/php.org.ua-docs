---
navigation:
  - imagick.getimagehistogram.md: '« Imagick::getImageHistogram'
  - imagick.getimageinterlacescheme.md: 'Imagick::getImageInterlaceScheme »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageIndex

(PECL imagick 2, PECL imagick 3)

Imagick::getImageIndex — Повертає індекс активного поточного зображення.

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::getImageIndex(): int
```

Повертає індекс активного поточного зображення в об'єкті Imagick. Цей метод оголошено застарілим. Використовуйте [Imagick::getIteratorIndex()](imagick.getiteratorindex.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що містить індекс зображення у стеку.

### Помилки

Викликає ImagickException у разі виникнення помилки.
