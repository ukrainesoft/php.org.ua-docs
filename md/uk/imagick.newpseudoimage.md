Створює нове зображення

-   [« Imagick::newImage](imagick.newimage.html)
    
-   [Imagick::nextImage »](imagick.nextimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює нове зображення
    

# Imagick::newPseudoImage

(PECL imagick 2, PECL imagick 3)

Imagick::newPseudoImage — Створює нове зображення

### Опис

```methodsynopsis
public Imagick::newPseudoImage(int $columns, int $rows, string $pseudoString): bool
```

Створює нове зображення за допомогою псевдоформатів ImageMagick.

### Список параметрів

`columns`

Стовпці у новому зображенні.

`rows`

Рядки у новому зображенні.

`pseudoString`

Рядок, що містить визначення псевдозображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::newPseudoImage()****

```php
<?php
function newPseudoImage($canvasType) {
    $imagick = new \Imagick();
    $imagick->newPseudoImage(300, 300, $canvasType);
    $imagick->setImageFormat("png");
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

//newPseudoImage('gradient:red-rgba(64, 255, 255, 0.5)');
//newPseudoImage("radial-gradient:red-blue");
newPseudoImage("plasma:fractal");

?>
```