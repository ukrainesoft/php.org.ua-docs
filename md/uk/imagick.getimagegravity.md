---
navigation:
  - imagick.getimagegeometry.md: '« Imagick::getImageGeometry'
  - imagick.getimagegreenprimary.md: 'Imagick::getImageGreenPrimary »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageGravity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageGravity

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::getImageGravity — Повертає значення гравітації (тяжіння)

### Опис

```methodsynopsis
public Imagick::getImageGravity(): int
```

Возвращает значение гравитации изображения. В отличие от[Imagick::getGravity()](imagick.getgravity.md), цей метод повертає гравітацію, встановлену для поточного зображення у послідовності. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.4 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Возвращает значение гравитации. Смотрите список[констант гравітації](imagick.constants.md#imagick.constants.gravity)
