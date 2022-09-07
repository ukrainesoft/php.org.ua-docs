---
navigation:
  - imagick.charcoalimage.md: '« Imagick::charcoalImage'
  - imagick.clampimage.md: 'Imagick::clampImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::chopImage'
---
# Imagick::chopImage

(PECL imagick 2, PECL imagick 3)

Imagick::chopImage — Видаляє область зображення та обрізає його.

### Опис

```methodsynopsis
public Imagick::chopImage(    int $width,    int $height,    int $x,    int $y): bool
```

Видалення вибраної області з реструктуризацією зображення.

### Список параметрів

`width`

Ширина області, що обрізається

`height`

Висота області, що обрізається

`x`

Початок обрізається по осі X

`y`

Початок обрізається по осі Y

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Використання **Imagick::chopImage()****

Приклад використання Imagick:: chopImage

```php
<?php
/* Создаём объекты */
$image = new Imagick();
$pixel = new ImagickPixel( 'gray' );

/* Новое изображение */
$image->newImage(400, 200, $pixel);

/* Обрезка изображения */
$image->chopImage(200, 200, 0, 0);

/* Установка формата изображения */
$image->setImageFormat('png');

/* Вывод изображения с заголовками */
header('Content-type: image/png');
echo $image;

?>
```

### Дивіться також

-   [Imagick::cropImage()](imagick.cropimage.md) - Витягує область зображення
