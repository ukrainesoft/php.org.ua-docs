Встановлює ітерацію зображення

-   [« Imagick::setImageInterpolateMethod](imagick.setimageinterpolatemethod.html)
    
-   [Imagick::setImageMatte »](imagick.setimagematte.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює ітерацію зображення
    

# Imagick::setImageIterations

(PECL imagick 2, PECL imagick 3)

Imagick::setImageIterations — Встановлює ітерацію зображення

### Опис

```methodsynopsis
public Imagick::setImageIterations(int $iterations): bool
```

Встановлює кількість ітерацій, коли анімоване зображення повторюється.

### Список параметрів

`iterations`

Число ітерацій, які зображення має повторити. Використовуйте '0' для безперервного повторення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageIterations()****

```php
<?php

$imagick = new Imagick(realpath("Test.gif"));

$imagick = $imagick->coalesceImages();
$imagick->setImageIterations(1);
$imagick = $imagick->deconstructImages();

$imagick->writeImages('/path/to/save/OnceOnly.gif', true);

?>
```