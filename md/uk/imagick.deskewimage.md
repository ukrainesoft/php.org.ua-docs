---
navigation:
  - imagick.deleteimageproperty.md: '« Imagick::deleteImageProperty'
  - imagick.despeckleimage.md: 'Imagick::despeckleImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::deskewImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::deskewImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3 >= 3.3.0)

Imagick::deskewImage — Видаляє перекіс із зображення.

### Опис

```methodsynopsis
public Imagick::deskewImage(float $threshold): bool
```

Метод можна використовувати для видалення перекосу, наприклад відсканованих зображень, якщо папір не був правильно розміщений на поверхні сканування. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`threshold`

Розмір перекосу

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Imagick::deskewImage()\*\*\*\*

```php
<?php
function deskewImage($threshold) {
    $imagick = new \Imagick(realpath("images/NYTimes-Page1-11-11-1918.jpg"));
    $deskewImagick = clone $imagick;

    //Это единственное, что требуется для удаления перекоса.
    $deskewImagick->deskewImage($threshold);

    //Остальная часть этого Приклада - сделать результат очевидным,
    //потому что в противном случае результат не очевиден.
    $trim = 9;

    $deskewImagick->cropImage($deskewImagick->getImageWidth() - $trim, $deskewImagick->getImageHeight(), $trim, 0);
    $imagick->cropImage($imagick->getImageWidth() - $trim, $imagick->getImageHeight(), $trim, 0);
    $deskewImagick->resizeimage($deskewImagick->getImageWidth() / 2, $deskewImagick->getImageHeight() / 2, \Imagick::FILTER_LANCZOS, 1);
    $imagick->resizeimage($imagick->getImageWidth() / 2, $imagick->getImageHeight() / 2, \Imagick::FILTER_LANCZOS, 1);
    $newCanvas = new \Imagick();
    $newCanvas->newimage($imagick->getImageWidth() + $deskewImagick->getImageWidth() + 20, $imagick->getImageHeight(), 'red', 'jpg');
    $newCanvas->compositeimage($imagick, \Imagick::COMPOSITE_COPY, 5, 0);
    $newCanvas->compositeimage($deskewImagick, \Imagick::COMPOSITE_COPY, $imagick->getImageWidth() + 10, 0);

    header("Content-Type: image/jpg");
    echo $newCanvas->getImageBlob();
}

?>
```
