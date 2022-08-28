Імітує фото Polaroid

-   [« Imagick::pingImageFile](imagick.pingimagefile.html)
    
-   [Imagick::posterizeImage »](imagick.posterizeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Імітує фото Polaroid
    

# Imagick::polaroidImage

(PECL imagick 2, PECL imagick 3)

Imagick::polaroidImage — Імітує фото Polaroid

### Опис

```methodsynopsis
public Imagick::polaroidImage(ImagickDraw $properties, float $angle): bool
```

Імітує фото Polaroid. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.2 або старшим.

### Список параметрів

`properties`

Властивості Polaroid.

`angle`

Кут Polaroid.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::polaroidImage()****

Приклад використання Imagick::polaroidImage()

```php
<?php
/* Создание объекта */
$image = new Imagick('source.png');

/* Установка непрозрачности */
$image->polaroidImage(new ImagickDraw(), 25);

/* Вывод изображения */
header('Content-type: image/png');
echo $image;

?>
```