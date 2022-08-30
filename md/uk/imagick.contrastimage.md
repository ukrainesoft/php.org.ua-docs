Змінює контраст зображення

-   [« Imagick::construct](imagick.construct.html)
    
-   [Imagick::contrastStretchImage »](imagick.contraststretchimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Змінює контраст зображення
    

# Imagick::contrastImage

(PECL imagick 2, PECL imagick 3)

Imagick::contrastImage — Змінює контраст зображення

### Опис

```methodsynopsis
public Imagick::contrastImage(bool $sharpen): bool
```

Збільшує різницю в інтенсивності між світлими та темними елементами зображення. Встановіть збільшення різкості на значення, відмінне від 0, щоб збільшити контраст зображення, інакше контраст зменшується.

### Список параметрів

`sharpen`

Значення різкості

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::contrastImage()****

```php
<?php
function contrastImage($imagePath, $contrastType) {
    $imagick = new \Imagick(realpath($imagePath));
    if ($contrastType != 2) {
        $imagick->contrastImage($contrastType);
    }

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```