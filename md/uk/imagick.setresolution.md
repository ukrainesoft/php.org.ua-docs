---
navigation:
  - imagick.setregistry.md: '« Imagick::setRegistry'
  - imagick.setresourcelimit.md: 'Imagick::setResourceLimit »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setResolution'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setResolution

(PECL imagick 2, PECL imagick 3)

Imagick::setResolution — Встановлює роздільну здатність зображення

### Опис

```methodsynopsis
public Imagick::setResolution(float $x_resolution, float $y_resolution): bool
```

Встановлює роздільну здатність зображення.

### Список параметрів

`x_resolution`

Горизонтальний дозвіл.

`y_resolution`

Вертикальна роздільна здатність.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Примітки

**Imagick::setResolution()** необхідно викликати перед завантаженням або створенням зображення.

### Дивіться також

-   [Imagick::setImageResolution()](imagick.setimageresolution.md) \- Встановлює роздільну здатність зображення
-   [Imagick::getImageResolution()](imagick.getimageresolution.md) \- Повертає роздільну здатність зображення за X і Y
