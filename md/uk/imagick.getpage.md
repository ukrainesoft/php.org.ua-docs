---
navigation:
  - imagick.getpackagename.md: '« Imagick::getPackageName'
  - imagick.getpixeliterator.md: 'Imagick::getPixelIterator »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getPage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getPage

(PECL imagick 2, PECL imagick 3)

Imagick::getPage — Повертає геометрію сторінки

### Опис

```methodsynopsis
public Imagick::getPage(): array
```

Повертає геометрію сторінки, пов'язану з об'єктом Imagick, у вигляді асоціативного масиву з ключами "width", "height", "x" та "y".

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає геометрію сторінки, пов'язану з об'єктом Imagick, у вигляді асоціативного масиву з ключами "width", "height", "x" та "y", у разі помилки викидає виняток ImagickException.
