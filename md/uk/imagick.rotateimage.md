Повертає зображення

-   [« Imagick::rollImage](imagick.rollimage.html)
    
-   [Imagick::rotationalBlurImage »](imagick.rotationalblurimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає зображення
    

# Imagick::rotateImage

(PECL imagick 2, PECL imagick 3)

Imagick::rotateImage — Повертає зображення

### Опис

```methodsynopsis
public Imagick::rotateImage(mixed $background, float $degrees): bool
```

Повертає зображення на вказану кількість градусів. Порожні трикутники, що залишилися від повороту зображення, заповнюються кольором тла.

### Список параметрів

`background`

Колір фону.

`degrees`

Кут повороту у градусах. Кут повороту інтерпретується як кількість градусів для повороту зображення за годинниковою стрілкою.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволено використання рядка, який представляє колір, як перший параметр. Попередні версії допускали лише об'єкт ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання **Imagick::rotateImage()****

```php
<?php
function rotateImage($imagePath, $angle, $color) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->rotateimage($color, $angle);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```