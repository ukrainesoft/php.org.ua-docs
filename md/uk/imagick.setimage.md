Замінює зображення в об'єкті

-   [« Imagick::setGravity](imagick.setgravity.html)
    
-   [Imagick::setImageAlphaChannel »](imagick.setimagealphachannel.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Замінює зображення в об'єкті
    

# Imagick::setImage

(PECL imagick 2, PECL imagick 3)

Imagick::setImage — Замінює зображення в об'єкті

### Опис

```methodsynopsis
public Imagick::setImage(Imagick $replace): bool
```

Замінює поточну послідовність зображень зображенням об'єкта, що замінює.

### Список параметрів

`replace`

Замінний об'єкт Imagick.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImage()****

Приклад використання Imagick::setImage()

```php
<?php
/* Создание объектов */
$image = new Imagick('source.jpg');
$replace = new Imagick('replace.jpg');

/* source.jpg заменяется на replace.jpg */
$image->setImage($replace);

/* Вывод изображения */
header('Content-type: image/jpeg');
echo $image;

?>
```