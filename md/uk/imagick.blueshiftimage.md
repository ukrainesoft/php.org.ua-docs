- [« Imagick::blackThresholdImage](imagick.blackthresholdimage.md)
- [Imagick::blurImage »](imagick.blurimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Опис

# Imagick::blueShiftImage

(PECL imagick 3 \>= 3.3.0)

Imagick::blueShiftImage — Опис

### Опис

public **Imagick::blueShiftImage**(float `$factor` = 1.5): bool

Приглушує кольори зображення для імітації сцени вночі при
місячному світлі.

### Список параметрів

`factor`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **Imagick::blueShiftImage()****

`<?phpfunction blueShiftImage($imagePath, $blueShift) {    $imagick = new \Imagick(realpath($imagePath)); $imagick->blueShiftImage($blueShift); header("Content-Type: image/jpg"); echo $imagick->getImageBlob();}?> `
