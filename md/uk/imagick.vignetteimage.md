---
navigation:
  - imagick.valid.md: '« Imagick::valid'
  - imagick.waveimage.md: 'Imagick::waveImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::vignetteImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::vignetteImage

(PECL imagick 2, PECL imagick 3)

Imagick::vignetteImage — Додає він'єтний фільтр до зображення

### Опис

```methodsynopsis
public Imagick::vignetteImage(    float $blackPoint,    float $whitePoint,    int $x,    int $y): bool
```

Пом'якшує краї зображення у стилі віньєтки. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`blackPoint`

Чорна точка

`whitePoint`

Біла точка

`x`

Зміщення еліпса по осі X

`y`

Зміщення еліпса по осі Y

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::vignetteImage()\*\*\*\*

```php
<?php
function vignetteImage($imagePath, $blackPoint, $whitePoint, $x, $y) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->vignetteImage($blackPoint, $whitePoint, $x, $y);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::waveImage()](imagick.waveimage.md) \- Застосовує хвильовий фільтр до зображення
-   [Imagick::swirlImage()](imagick.swirlimage.md) \- Закручує пікселі навколо центру зображення
