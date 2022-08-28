Застосовує цифровий фільтр

-   [« Imagick::matteFloodfillImage](imagick.mattefloodfillimage.html)
    
-   [Imagick::mergeImageLayers »](imagick.mergeimagelayers.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Застосовує цифровий фільтр
    

# Imagick::medianFilterImage

(PECL imagick 2, PECL imagick 3)

Imagick::medianFilterImage — Застосовує цифровий фільтр

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::medianFilterImage(float $radius): bool
```

Застосовує цифровий фільтр, який покращує якість зображення з шумом. Кожен піксель замінюється медіаною у наборі сусідніх пікселів, що визначаються радіусом.

### Список параметрів

`radius`

Радіус сусідніх пікселів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::medianFilterImage()****

```php
<?php
function medianFilterImage($radius, $imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    @$imagick->medianFilterImage($radius);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```