- [« Imagick::setCompression](imagick.setcompression.md)
- [Imagick::setFilename »](imagick.setfilename.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Встановлює якість стиснення об'єкта за замовчуванням

# Imagick::setCompressionQuality

(PECL imagick 2, PECL imagick 3)

Imagick::setCompressionQuality — Встановлює якість стиснення об'єкта
за замовчуванням

### Опис

public **Imagick::setCompressionQuality**(int `$quality`): bool

Встановлює якість стандартного стиснення об'єкта.

**Застереження**

Цей метод працює тільки для нових зображень, наприклад, створених з
допомогою Imagick::newPseudoImage. Для існуючих зображень слід
використовувати
[Imagick::setImageCompressionQuality()](imagick.setimagecompressionquality.md).

### Список параметрів

`quality`
Ціле число (int) від 1 до 100, 1 = високий рівень стиснення, 100 = низький
ступінь стиснення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **Imagick::setCompressionQuality()****

`<?phpfunction setCompressionQuality($imagePath, $quality) {    $backgroundImagick = new \Imagick(realpath($imagePath)); $imagick==newImagick(); $imagick->setCompressionQuality($quality); $imagick->newPseudoImage(        $backgroundImagick->getImageWidth(),        $backgroundImagick->getImageHeight(),                      $imagick->compositeImage(        $backgroundImagick,        \Imagick::COMPOSITE_ATOP,         0,                      | $imagick->setFormat("jpg"); header("Content-Type: image/jpg"); echo $imagick->getImageBlob();}?> `
