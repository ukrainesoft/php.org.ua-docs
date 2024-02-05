---
navigation:
  - imagick.thumbnailimage.md: '« Imagick::thumbnailImage'
  - imagick.tostring.md: 'Imagick::\_\_toString »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::tintImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::tintImage

(PECL imagick 2, PECL imagick 3)

Imagick::tintImage — Застосовує вектор кольору до кожного пікселя зображення

### Опис

```methodsynopsis
public Imagick::tintImage(mixed $tint, mixed $opacity, bool $legacy = false): bool
```

Застосовує вектор кольору до кожного пікселя зображення. Довжина вектора дорівнює 0 для чорного та білого та максимальна довжина для півтонів. Функція векторного зважування: f(x)=(1-(4.0)\*((x-0.5)\*(x-0.5)))).

### Список параметрів

`tint`

`opacity`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє рядок, що представляє колір, як перший параметр і число з точкою, що представляє значення непрозорості, як другий параметр. Попередні версії допускали лише об'єкти ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання** Imagick::tintImage()\*\*\*\*

```php
<?php
function tintImage($r, $g, $b, $a) {
    $a = $a / 100;

    $imagick = new \Imagick();
    $imagick->newPseudoImage(400, 400, 'gradient:black-white');

    $tint = new \ImagickPixel("rgb($r, $g, $b)");
    $opacity = new \ImagickPixel("rgb(128, 128, 128, $a)");
    $imagick->tintImage($tint, $opacity);
    $imagick->setImageFormat('png');
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
