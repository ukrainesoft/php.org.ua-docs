Тонування зображення сепією

-   [« Imagick::separateImageChannel](imagick.separateimagechannel.html)
    
-   [Imagick::setBackgroundColor »](imagick.setbackgroundcolor.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Тонування зображення сепією
    

# Imagick::sepiaToneImage

(PECL imagick 2, PECL imagick 3)

Imagick::sepiaToneImage — Тонування зображення сепією

### Опис

```methodsynopsis
public Imagick::sepiaToneImage(float $threshold): bool
```

Застосовує до зображення спеціальний ефект, аналогічний ефекту, що досягається фотолабораторії за допомогою тонування сепією. Поріг варіюється від 0 до QuantumRange і є мірою тонування сепії. Поріг 80 - відправна точка для розумного тону.

### Список параметрів

`threshold`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::sepiaToneImage()****

```php
<?php
function sepiaToneImage($imagePath, $sepia) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->sepiaToneImage($sepia);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```