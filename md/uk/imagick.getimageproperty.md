---
navigation:
  - imagick.getimageproperties.html: '« Imagick::getImageProperties'
  - imagick.getimageredprimary.html: 'Imagick::getImageRedPrimary »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::getImageProperty'
---
# Imagick::getImageProperty

(PECL imagick 2, PECL imagick 3)

Imagick::getImageProperty — Повертає назву зображення.

### Опис

```methodsynopsis
public Imagick::getImageProperty(string $name): string
```

Повертає іменовану властивість зображення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.2 або старшим.

### Список параметрів

`name`

Ім'я властивості (наприклад, Exif: DateTime).

### Значення, що повертаються

Повертає рядок, що містить властивість зображення, або false, якщо властивість із заданим ім'ям не існує.

### Приклади

**Приклад #1 Приклад використання **Imagick::getImageProperty()****

Завдання та отримання властивості зображення

```php
<?php
$image = new Imagick();
$image->newImage(300, 200, "black");

$image->setImageProperty('Exif:Make', 'Imagick');
echo $image->getImageProperty('Exif:Make');
?>
```

### Дивіться також

-   [Imagick::setImageProperty()](imagick.setimageproperty.html) - Встановлює властивість зображення
