---
navigation:
  - imagick.exportimagepixels.md: '« Imagick::exportImagePixels'
  - imagick.filter.md: 'Imagick::filter »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::extentImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::extentImage

(PECL imagick 2, PECL imagick 3)

Imagick::extentImage — Встановлює розмір зображення

### Опис

```methodsynopsis
public Imagick::extentImage(    int $width,    int $height,    int $x,    int $y): bool
```

Зручний спосіб встановлення розміру зображення. Метод встановлює розмір зображення і дозволяє встановити координати x,y там, де починається нова область. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.1 або старшим.

**Застереження**

До ImageMagick 6.5.7-8 (1623) значення $x було позитивним при зсуві вліво і негативним при зсуві вправо, а значення $y було позитивним при зрушенні зображення вгору і негативним при зсуві зображення вниз. Десь між ImageMagick 6.3.7 (1591) та ImageMagick 6.5.7-8 (1623) осі $x і $y були перевернуті так, що значення $x було негативним при зрушенні вліво і позитивним при зрушенні вправо, а значення $y було негативним при зрушенні зображення нагору і позитивним при зсуві зображення вниз. Десь між ImageMagick 6.5.7-8 (1623) та ImageMagick 6.6.9-7 (1641) осі $x і $y були повернуті назад до функціональності до ImageMagick 6.5.7-8 (1623).

### Список параметрів

`width`

Нова ширина.

`height`

Нова висота.

`x`

Позиція X для нового розміру.

`y`

Позиція Y для нового розміру.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::resizeImage()](imagick.resizeimage.md) \- Масштабує зображення
-   [Imagick::thumbnailImage()](imagick.thumbnailimage.md) \- Змінює розмір зображення
-   [Imagick::cropImage()](imagick.cropimage.md) \- Витягує область зображення
