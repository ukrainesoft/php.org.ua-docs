---
navigation:
  - imagick.colorizeimage.md: '« Imagick::colorizeImage'
  - imagick.combineimages.md: 'Imagick::combineImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::colorMatrixImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::colorMatrixImage

(PECL imagick 3 >= 3.3.0)

Imagick::colorMatrixImage — Застосовує перетворення кольору до зображення

### Опис

```methodsynopsis
public Imagick::colorMatrixImage(array $color_matrix = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує перетворення кольору до зображення. Цей метод дозволяє змінювати насиченість, обертання відтінку, яскравість альфа-каналу та інші ефекти. Хоча можна використовувати матриці перетворення змінного розміру, зазвичай використовується матриця 5x5 для RGBA зображення і матриця 6x6 для CMYKA (або RGBA зі зміщеннями). Матриця аналогічна матрицям, які використовуються в Adobe Flash, за винятком того, що зміщення вказані в стовпці 6, а не 5 (для підтримки зображень CMYKA), а зміщення нормалізовані (зсув Flash ділиться на 255).

### Список параметрів

`color_matrix`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::colorMatrixImage()\*\*\*\*

```php
<?php
function colorMatrixImage($imagePath, $colorMatrix) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageOpacity(1);

    //Цветовая матрица должна выглядеть так:
    //    $colorMatrix = [
    //        1.5, 0.0, 0.0, 0.0, 0.0, -0.157,
    //        0.0, 1.0, 0.5, 0.0, 0.0, -0.157,
    //        0.0, 0.0, 1.5, 0.0, 0.0, -0.157,
    //        0.0, 0.0, 0.0, 1.0, 0.0,  0.0,
    //        0.0, 0.0, 0.0, 0.0, 1.0,  0.0,
    //        0.0, 0.0, 0.0, 0.0, 0.0,  1.0
    //    ];

    $background = new \Imagick();
    $background->newPseudoImage($imagick->getImageWidth(), $imagick->getImageHeight(),  "pattern:checkerboard");

    $background->setImageFormat('png');

    $imagick->setImageFormat('png');
    $imagick->colorMatrixImage($colorMatrix);

    $background->compositeImage($imagick, \Imagick::COMPOSITE_ATOP, 0, 0);

    header("Content-Type: image/png");
    echo $background->getImageBlob();
}

?>
```
