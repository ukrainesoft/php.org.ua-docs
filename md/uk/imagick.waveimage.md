Застосовує хвильовий фільтр до зображення

-   [« Imagick::vignetteImage](imagick.vignetteimage.html)
    
-   [Imagick::whiteThresholdImage »](imagick.whitethresholdimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Застосовує хвильовий фільтр до зображення
    

# Imagick::waveImage

(PECL imagick 2, PECL imagick 3)

Imagick::waveImage — Застосовує хвильовий фільтр до зображення

### Опис

```methodsynopsis
public Imagick::waveImage(float $amplitude, float $length): bool
```

Застосовує хвильовий фільтр зображення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`amplitude`

Амплітуда хвилі.

`length`

Довжина хвилі.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 WaveImage може бути досить повільним **Imagick::waveImage()****

```php
<?php
function waveImage($imagePath, $amplitude, $length) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->waveImage($amplitude, $length);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::solarizeImage()](imagick.solarizeimage.html) - Застосовує до зображення ефект соляризації
-   [Imagick::oilpaintImage()](imagick.oilpaintimage.html) - Імітує картину олією
-   [Imagick::embossImage()](imagick.embossimage.html) - Повертає зображення у градаціях сірого з тривимірним ефектом
-   [Imagick::addNoiseImage()](imagick.addnoiseimage.html) - Накладає випадковий шум на зображення
-   [Imagick::swirlImage()](imagick.swirlimage.html) - Закручує пікселі навколо центру зображення