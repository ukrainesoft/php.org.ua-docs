Додає адаптивний фільтр розмиття до зображення

-   [« Imagick](class.imagick.html)
    
-   [Imagick::adaptiveResizeImage »](imagick.adaptiveresizeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Додає адаптивний фільтр розмиття до зображення
    

# Imagick::adaptiveBlurImage

(PECL imagick 2, PECL imagick 3)

Imagick::adaptiveBlurImage — Додає адаптивний фільтр розмиття до зображення

### Опис

```methodsynopsis
public Imagick::adaptiveBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Додає адаптивний фільтр розмиття до зображення. Інтенсивність адаптивного розмиття значно зменшується до країв зображення, тоді як стандартне розмиття рівномірно розподіляється по всьому зображенню. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`radius`

Радіус Гауса, у пікселях, крім центрального пікселя. Якщо передано 0, то радіус буде вибрано автоматично.

`sigma`

Стандартне відхилення Гауса, у пікселях.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::adaptiveBlurImage()****

Адаптивне розмиття зображення та відображення його у браузері.

```php
<?php

header('Content-type: image/jpeg');

$image = new Imagick('test.jpg');

$image->adaptiveBlurImage(5,3);
echo $image;

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад висновку: Використання Imagick::adaptiveBlurImage()](images/c0d23d2d6769e53e24a1b3136c064577-adaptiveBlurImage.gif)

### Дивіться також

-   [Imagick::blurImage()](imagick.blurimage.html) - Додає фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.html) - Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.html) - Радіальне розмиття зображення