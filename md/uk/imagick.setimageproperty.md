Встановлює властивість зображення

-   [« Imagick::setImageProfile](imagick.setimageprofile.html)
    
-   [Imagick::setImageRedPrimary »](imagick.setimageredprimary.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює властивість зображення
    

# Imagick::setImageProperty

(PECL imagick 2, PECL imagick 3)

Imagick::setImageProperty — Встановлює властивість зображення

### Опис

```methodsynopsis
public Imagick::setImageProperty(string $name, string $value): bool
```

Встановлює іменовану властивість зображення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.2 або старшим.

### Список параметрів

`name`

`value`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageProperty()****

Встановлення та отримання властивостей зображення

```php
<?php
$image = new Imagick();
$image->newImage(300, 200, "black");

$image->setImageProperty('Exif:Make', 'Imagick');
echo $image->getImageProperty('Exif:Make');
?>
```

### Дивіться також

-   [Imagick::getImageProperty()](imagick.getimageproperty.html) - Повертає іменовану властивість зображення