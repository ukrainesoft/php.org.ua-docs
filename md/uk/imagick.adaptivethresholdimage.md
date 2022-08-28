Вибір порога кожного пікселя в залежності від діапазону інтенсивності

-   [« Imagick::adaptiveSharpenImage](imagick.adaptivesharpenimage.html)
    
-   [Imagick::addImage »](imagick.addimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Вибір порога кожного пікселя в залежності від діапазону інтенсивності
    

# Imagick::adaptiveThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::adaptiveThresholdImage — Вибір порога кожного пікселя в залежності від діапазону інтенсивності.

### Опис

```methodsynopsis
public Imagick::adaptiveThresholdImage(int $width, int $height, int $offset): bool
```

Вибір індивідуального обмеження кожного пікселя в залежності від діапазону значень інтенсивності навколо цього пікселя. Це дає можливість встановити поріг зображення, в якому гістограма глобальної інтенсивності не містить відмітних піків.

### Список параметрів

`width`

Область сусідів за шириною.

`height`

Область сусідів висотою.

`offset`

Середнє зміщення

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::adaptiveThresholdImage()****

```php
<?php
function adaptiveThresholdImage($imagePath, $width, $height, $adaptiveOffset) {
    $imagick = new \Imagick(realpath($imagePath));
    $adaptiveOffsetQuantum = intval($adaptiveOffset * \Imagick::getQuantum());
    $imagick->adaptiveThresholdImage($width, $height, $adaptiveOffsetQuantum);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```