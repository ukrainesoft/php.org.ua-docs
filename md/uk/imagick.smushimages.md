---
navigation:
  - imagick.sketchimage.md: '« Imagick::sketchImage'
  - imagick.solarizeimage.md: 'Imagick::solarizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::smushImages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::smushImages

(PECL imagick 3 >= 3.3.0)

Imagick::smushImages — Виберіть усі зображення з поточного покажчика зображення до кінця списку зображень та переміщує їх.

### Опис

```methodsynopsis
public Imagick::smushImages(bool $stack, int $offset): Imagick
```

Бере всі зображення з поточного покажчика зображення в кінець списку зображень і переміщує їх один до одного зверху вниз, якщо параметру stack встановлено значення true, інакше - зліва направо.

### Список параметрів

`stack`

`offset`

### Значення, що повертаються

Нове розмите зображення.

### Приклади

**Приклад #1 Приклад використання** Imagick::smushImages()\*\*\*\*

```php
<?php
function smushImages($imagePath, $imagePath2) {

    $imagick = new \Imagick(realpath($imagePath));
    $imagick2 = new \Imagick(realpath($imagePath2));

    $imagick->addimage($imagick2);
    $smushed = $imagick->smushImages(false, 50);
    $smushed->setImageFormat('jpg');
    header("Content-Type: image/jpg");
    echo $smushed->getImageBlob();
}

?>
```
