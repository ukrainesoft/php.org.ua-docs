Перекласти всі пікселі нижче граничного значення в чорний колір

-   [« Imagick::averageImages](imagick.averageimages.md)
    
-   [Imagick::blueShiftImage »](imagick.blueshiftimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Перекласти всі пікселі нижче граничного значення в чорний колір
    

# Imagick::blackThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::blackThresholdImage — Перекласти всі пікселі нижче граничного значення в чорний колір

### Опис

```methodsynopsis
public Imagick::blackThresholdImage(mixed $threshold): bool
```

Працює так само, як Imagick::thresholdImage(), але змінюються тільки пікселі нижче порогового значення, тоді як інші пікселі залишаються незмінними.

### Список параметрів

`threshold`

Порогове значення нижче якого всі пікселі стануть чорними

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия             | Описание                                                                                                  |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| PECL imagick 2.1.0 | Як параметр можна передавати колір рядком. У попередніх версіях дозволялося передавати лише ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання **Imagick::blackThresholdImage()****

```php
<?php
function blackThresholdImage($imagePath, $thresholdColor) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->blackthresholdimage($thresholdColor);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```