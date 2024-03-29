---
navigation:
  - imagick.linearstretchimage.md: '« Imagick::linearStretchImage'
  - imagick.listregistry.md: 'Imagick::listRegistry »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::liquidRescaleImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::liquidRescaleImage

(PECL imagick 2 >= 2.2.0, PECL imagick 3)

Imagick::liquidRescaleImage — Анімує зображення або зображення

### Опис

```methodsynopsis
public Imagick::liquidRescaleImage(    int $width,    int $height,    float $delta_x,    float $rigidity): bool
```

Масштабує зображення за допомогою методу liquid rescaling. Він є реалізацією техніки seam carving. Щоб метод працював належним чином, ImageMagick має бути скомпільований за допомогою liblqr. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`width`

Ширина цільового розміру.

`height`

Висота цільового розміру.

`delta_x`

Визначає скільки шов може проходити по осі x. Під час передачі значення 0 шви стають прямими.

`rigidity`

Вводить ухил для непрямих швів. Цей параметр зазвичай дорівнює 0.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::resizeImage()](imagick.resizeimage.md) \- Масштабує зображення
