---
navigation:
  - imagick.setimageprofile.md: '« Imagick::setImageProfile'
  - imagick.setimageredprimary.md: 'Imagick::setImageRedPrimary »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageProperty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Приклад #1 Приклад використання** Imagick::setImageProperty()\*\*\*\*

Встановлення та отримання властивостей зображення

```php
<?php
$image = new Imagick();
$image->newImage(300, 200, "black");

$image->setImageProperty('Exif:Make', 'Imagick');
echo $image->getImageProperty('Exif:Make');
?>
```

### Дивіться також

-   [Imagick::getImageProperty()](imagick.getimageproperty.md) \- Повертає іменовану властивість зображення
