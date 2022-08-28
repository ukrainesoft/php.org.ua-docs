Різкість зображення

-   [« Imagick::uniqueImageColors](imagick.uniqueimagecolors.html)
    
-   [Imagick::valid »](imagick.valid.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Різкість зображення
    

# Imagick::unsharpMaskImage

(PECL imagick 2, PECL imagick 3)

Imagick::unsharpMaskImage — Різкість зображення

### Опис

```methodsynopsis
public Imagick::unsharpMaskImage(    float $radius,    float $sigma,    float $amount,    float $threshold,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Різкість зображення. Ми згортаємо зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (сигма). Для отримання розумних результатів радіус має бути більшим за сигму. Вкажіть радіус 0, щоб Imagick::UnsharpMaskImage() поставив відповідний радіус автоматично.

### Список параметрів

`radius`

`sigma`

`amount`

`threshold`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::unsharpMaskImage()****

```php
<?php
function unsharpMaskImage($imagePath, $radius, $sigma, $amount, $unsharpThreshold) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->unsharpMaskImage($radius, $sigma, $amount, $unsharpThreshold);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```