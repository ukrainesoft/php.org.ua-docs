---
navigation:
  - imagick.setimagechanneldepth.md: '« Imagick::setImageChannelDepth'
  - imagick.setimagecolormapcolor.md: 'Imagick::setImageColormapColor »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageClipMask'
---
# Imagick::setImageClipMask

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::setImageClipMask — Встановлює маску кліпу

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageClipMask(Imagick $clip_mask): bool
```

Встановлює маску зображення з іншого об'єкта Imagick. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`clip_mask`

Об'єкт Imagick, що містить маску кліпу

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageClipMask()****

```php
<?php
function setImageClipMask($imagePath) {
    $imagick = new \Imagick();
    $imagick->readImage(realpath($imagePath));

    $width = $imagick->getImageWidth();
    $height = $imagick->getImageHeight();

    $clipMask = new \Imagick();
    $clipMask->newPseudoImage(
        $width,
        $height,
        "canvas:transparent"
    );

    $draw = new \ImagickDraw();
    $draw->setFillColor('white');
    $draw->circle(
        $width / 2,
        $height / 2,
        ($width / 2) + ($width / 4),
        $height / 2
    );
    $clipMask->drawImage($draw);
    $imagick->setImageClipMask($clipMask);

    $imagick->negateImage(false);
    $imagick->setFormat("png");

    header("Content-Type: image/png");
    echo $imagick->getImagesBlob();

}

?>
```
