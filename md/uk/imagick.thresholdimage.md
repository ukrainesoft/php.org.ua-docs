Змінює окремі пікселі на основі порогового значення

-   [« Imagick::textureImage](imagick.textureimage.md)
    
-   [Imagick::thumbnailImage »](imagick.thumbnailimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Змінює окремі пікселі на основі порогового значення
    

# Imagick::thresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::thresholdImage — Змінює окремі пікселі на основі порогового значення

### Опис

```methodsynopsis
public Imagick::thresholdImage(float $threshold, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює окремі пікселі залежно від їхньої інтенсивності в порівнянні з пороговим значенням. Результатом буде високо-контрастне, двоколірне зображення.

### Список параметрів

`threshold`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::thresholdImage()****

```php
<?php
function thresholdimage($imagePath, $threshold, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->thresholdimage($threshold * \Imagick::getQuantum(), $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```