Зафарбовує всі пікселі вище за поріг у білий

-   [« Imagick::waveImage](imagick.waveimage.html)
    
-   [Imagick::writeImage »](imagick.writeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Зафарбовує всі пікселі вище за поріг у білий
    

# Imagick::whiteThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::whiteThresholdImage — Зафарбовує всі пікселі вище за поріг у білий

### Опис

```methodsynopsis
public Imagick::whiteThresholdImage(mixed $threshold): bool
```

Схожий на Imagick::ThresholdImage(), але зафарбовує всі пікселі вище за поріг у білий колір, залишаючи всі пікселі нижче порога без змін.

### Список параметрів

`threshold`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия             | Описание                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------|
| PECL imagick 2.1.0 | Тепер дозволяється передавати рядок, який представляє колір як параметр. Попередні версії допускають лише об'єкт ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання **Imagick::whiteThresholdImage()****

```php
<?php
function whiteThresholdImage($imagePath, $color) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->whiteThresholdImage($color);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```