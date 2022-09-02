---
navigation:
  - imagick.setimagegamma.md: '« Imagick::setImageGamma'
  - imagick.setimagegreenprimary.md: 'Imagick::setImageGreenPrimary »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageGravity'
---
# Imagick::setImageGravity

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::setImageGravity — Встановлює гравітацію зображення

### Опис

```methodsynopsis
public Imagick::setImageGravity(int $gravity): bool
```

Встановлює якість гравітації для поточного зображення. Метод можна використовувати для встановлення якості гравітації однієї послідовності зображень. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.4 або старшим.

### Список параметрів

`gravity`

Властивість гравітації. Зверніться до списку [gravity констант](imagick.constants.md#imagick.constants.gravity)

### Значення, що повертаються

Функція не повертає значення після виконання.
