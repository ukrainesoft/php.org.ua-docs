---
navigation:
  - imagick.getimagechannelstatistics.md: '« Imagick::getImageChannelStatistics'
  - imagick.getimagecolormapcolor.md: 'Imagick::getImageColormapColor »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageClipMask'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageClipMask

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::getImageClipMask — Повертає відсічну маску зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::getImageClipMask(): Imagick
```

Повертає відсічну маску зображення. Відсічна маска - об'єкт Imagick, що містить відсічні маски. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт Imagick, що містить відсічні маски.

### Помилки

Викликає ImagickException у разі виникнення помилки.
