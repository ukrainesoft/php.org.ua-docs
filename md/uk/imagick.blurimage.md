Додає фільтр розмиття до зображення

-   [« Imagick::blueShiftImage](imagick.blueshiftimage.md)
    
-   [Imagick::borderImage »](imagick.borderimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Додає фільтр розмиття до зображення
    

# Imagick::blurImage

(PECL imagick 2, PECL imagick 3)

Imagick::blurImage — Додає фільтр розмиття до зображення

### Опис

```methodsynopsis
public Imagick::blurImage(float $radius, float $sigma, int $channel = ?): bool
```

Додає фільтр розмиття до зображення. Необов'язковий третій параметр використовується для розмиття певного каналу.

### Список параметрів

`radius`

Радіус розмиття

`sigma`

Стандартне відхилення

`channel`

Константа [Channeltype](imagick.constants.html#imagick.constants.channel). Якщо не вказано, будуть розмиті всі канали.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::blurImage()****

Розмиття зображення та надсилання його до браузера.

```php
<?php

header('Content-type: image/jpeg');

$image = new Imagick('test.jpg');

$image->blurImage(5,3);
echo $image;

?>
```

### Дивіться також

-   [Imagick::adaptiveBlurImage()](imagick.adaptiveblurimage.md) - Додає адаптивний фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.md) - Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.md) - Радіальне розмиття зображення