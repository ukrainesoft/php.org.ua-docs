- [« Imagick::medianFilterImage](imagick.medianfilterimage.md)
- [Imagick::minifyImage »](imagick.minifyimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Об'єднує шари зображення

# Imagick::mergeImageLayers

(PECL imagick 2 \>= 2.1.0, PECL imagick 3)

Imagick::mergeImageLayers — Об'єднує шари зображення

### Опис

public **Imagick::mergeImageLayers**(int `$layer_method`):
[Imagick](class.imagick.md)

Об'єднує шари зображення на один. Метод корисний під час роботи з форматами
зображень, у яких використовується кілька шарів, наприклад, PSD.
Об'єднання контролюється за допомогою `layer_method`, який визначає
Метод об'єднання шарів. Цей метод доступний, якщо Imagick був
скомпільований з версією ImageMagick 6.3.7 або старшим.

### Список параметрів

`layer_method`
Одна із констант **`Imagick::LAYERMETHOD_*`**.

### Значення, що повертаються

Повертає об'єкт Imagick, що містить зображення.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::mergeImageLayers()****

` <?phpfunction mergeImageLayers($layerMethodType, $imagePath1, $imagePath2) {   $imagick = new \Imagick(realpath($imagePath)); $imagick2 = new \Imagick(realpath($imagePath2)); $imagick->addImage($imagick2); $imagick->setImageFormat('png'); $result==$imagick->mergeImageLayers($layerMethodType); header("Content-Type: image/png"); echo $result->getImageBlob();}?> `

### Дивіться також

- [Imagick::flattenImages()](imagick.flattenimages.md) - Об'єднує
послідовність зображень
