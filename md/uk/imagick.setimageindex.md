---
navigation:
  - imagick.setimagegreenprimary.md: '« Imagick::setImageGreenPrimary'
  - imagick.setimageinterlacescheme.md: 'Imagick::setImageInterlaceScheme »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageIndex

(PECL imagick 2, PECL imagick 3)

Imagick::setImageIndex — Встановлює позицію ітератора

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageIndex(int $index): bool
```

Встановлює ітератор у позицію списку зображень, вказану параметром index.

Цей метод оголошено застарілим. Використовуйте [Imagick::setIteratorIndex()](imagick.setiteratorindex.md)

### Список параметрів

`index`

Позиція встановлення ітератора.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
