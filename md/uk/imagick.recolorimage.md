Перефарбовує зображення

-   [« Imagick::readimages](imagick.readimages.html)
    
-   [Imagick::reduceNoiseImage »](imagick.reducenoiseimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перефарбовує зображення
    

# Imagick::recolorImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::recolorImage — Перефарбовує зображення

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::recolorImage(array $matrix): bool
```

Перетворення, масштабування, зсув або поворот кольорів зображення. Метод підтримує матриці змінного розміру, але матриця 5x5 зазвичай використовується для RGBA, а 6x6 - для CMYK. Останній рядок має містити нормалізовані значення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`matrix`

Матриця, яка містить значення кольору.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::recolorImage()****

```php
<?php
function recolorImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $remapColor = [ 1, 0, 0,
        0, 0, 1,
        0, 1, 0,];

//$remapColor = [
//    1.438, -0.122, -0.016,  0, 0, -0.03,
//    -0.062,  1.378, -0.016,  0, 0,  0.05,
//    -0.062, -0.122, 1.483,   0, 0, -0.02,
//];

    @$imagick->recolorImage($remapColor);

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::displayImage()](imagick.displayimage.html) - Виводить зображення