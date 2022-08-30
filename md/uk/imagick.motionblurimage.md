Імітує розмиття у русі

-   [« Imagick::mosaicImages](imagick.mosaicimages.md)
    
-   [Imagick::negateImage »](imagick.negateimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Імітує розмиття у русі
    

# Imagick::motionBlurImage

(PECL imagick 2, PECL imagick 3)

Imagick::motionBlurImage — Імітує розмиття в русі

### Опис

```methodsynopsis
public Imagick::motionBlurImage(    float $radius,    float $sigma,    float $angle,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Імітує розмиття у русі. Згортає зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (сигма). Для отримання розумних результатів радіус має бути більшим за сигму. Використовуйте радіус 0, і MotionBlurImage() вибере відповідний радіус самостійно. Кут задає кут розмиття руху.

### Список параметрів

`radius`

Радіус гауссіани в пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення Гауса в пікселях.

`angle`

Застосування ефекту під цим кутом.

`channel`

Вкажіть будь-яку константу каналу, яка є дійсною для вашого режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до списку [констант канала](imagick.constants.html#imagick.constants.channel). Аргумент каналу впливає лише в тому випадку, якщо Imagick скомпільовано з ImageMagick версії 6.4.4 або вище.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::motionBlurImage()****

```php
<?php
function motionBlurImage($imagePath, $radius, $sigma, $angle, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->motionBlurImage($radius, $sigma, $angle, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}
?>
```