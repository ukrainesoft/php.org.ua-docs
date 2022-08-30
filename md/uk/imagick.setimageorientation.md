Встановлює орієнтацію зображення

-   [« Imagick::setImageOpacity](imagick.setimageopacity.md)
    
-   [Imagick::setImagePage »](imagick.setimagepage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Встановлює орієнтацію зображення
    

# Imagick::setImageOrientation

(PECL imagick 2, PECL imagick 3)

Imagick::setImageOrientation — Встановлює орієнтацію зображення

### Опис

```methodsynopsis
public Imagick::setImageOrientation(int $orientation): bool
```

Встановлює орієнтацію зображення.

### Список параметрів

`orientation`

Одна з констант [ORIENTATION](imagick.constants.html#imagick.constants.orientation)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageOrientation()****

```php
<?php
// Кажется, ничего не делает
function setImageOrientation($imagePath, $orientationType) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageOrientation($orientationType);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```