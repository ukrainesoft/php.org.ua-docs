---
navigation:
  - imagick.distortimage.md: '« Imagick::distortImage'
  - imagick.edgeimage.md: 'Imagick::edgeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::drawImage'
---
# Imagick::drawImage

(PECL imagick 2, PECL imagick 3)

Imagick::drawImage — Рендеринг об'єкту ImagickDraw на поточному зображенні.

### Опис

```methodsynopsis
public Imagick::drawImage(ImagickDraw $draw): bool
```

Виконує рендеринг об'єкта ImagickDraw на поточному зображенні.

### Список параметрів

`draw`

Операції малювання, які виконуються до зображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
