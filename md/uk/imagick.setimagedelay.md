Встановлює затримку зображення

-   [« Imagick::setImageCompressionQuality](imagick.setimagecompressionquality.md)
    
-   [Imagick::setImageDepth »](imagick.setimagedepth.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Встановлює затримку зображення
    

# Imagick::setImageDelay

(PECL imagick 2, PECL imagick 3)

Imagick::setImageDelay — Встановлює затримку зображення

### Опис

```methodsynopsis
public Imagick::setImageDelay(int $delay): bool
```

Встановлює затримку зображення. Для анімованого зображення це кількість часу, протягом якого цей кадр зображення повинен відображатись до відображення наступного кадру.

Затримка може бути встановлена ​​індивідуально для кожного кадру зображення.

### Список параметрів

`delay`

Кількість часу, виражена в 'тиках', для якого має відображатися зображення. Для анімованих GIF-файлів є 100 тиків на секунду, тому значення 20 дорівнюватиме 20/100 секунди, тобто 1/5 секунди.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Змінити анімований GIF за допомогою **Imagick::setImageDelay()****

```php
<?php

// Измените анимированный GIF, чтобы его кадры воспроизводились с переменной скоростью,
// варьируясь от показа в течение 50 мс до 0 мс,
// что приведёт к пропуску фрейма в большинстве браузеров.
$imagick = new Imagick(realpath("Test.gif"));
$imagick = $imagick->coalesceImages();

$frameCount = 0;

foreach ($imagick as $frame) {
    $imagick->setImageDelay((($frameCount % 11) * 5));
    $frameCount++;
}

$imagick = $imagick->deconstructImages();

$imagick->writeImages("/path/to/save/output.gif", true);

?>
```