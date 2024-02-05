---
navigation:
  - imagick.forwardfouriertransformimage.md: '« Imagick::forwardFourierTransformImage'
  - imagick.functionimage.md: 'Imagick::functionImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::frameImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::frameImage

(PECL imagick 2, PECL imagick 3)

Imagick::frameImage — Додає імітацію тривимірного кордону

### Опис

```methodsynopsis
public Imagick::frameImage(    mixed $matte_color,    int $width,    int $height,    int $inner_bevel,    int $outer_bevel): bool
```

Додає імітацію тривимірної межі навколо зображення. Ширина та висота визначають ширину межі вертикальної та горизонтальної сторін рамки. Внутрішній та зовнішній скоси вказують ширину внутрішньої та зовнішньої тіні рамки.

### Список параметрів

`matte_color`

Об'єкт ImagickPixel або рядок, який представляє матовий колір.

`width`

Ширина кордону.

`height`

Висота кордону.

`inner_bevel`

Ширина внутрішнього скосу.

`outer_bevel`

Ширина зовнішнього скосу.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як перший. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |

### Приклади

**Пример #1 Пример использования**Imagick::frameImage()\*\*\*\*

```php
<?php
function frameImage($imagePath, $color, $width, $height, $innerBevel, $outerBevel) {
    $imagick = new \Imagick(realpath($imagePath));

    $width = $width + $innerBevel + $outerBevel;
    $height = $height + $innerBevel + $outerBevel;

    $imagick->frameimage(
        $color,
        $width,
        $height,
        $innerBevel,
        $outerBevel
    );
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
