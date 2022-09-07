---
navigation:
  - imagick.animateimages.md: '« Imagick::animateImages'
  - imagick.appendimages.md: 'Imagick::appendImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::annotateImage'
---
# Imagick::annotateImage

(PECL imagick 2, PECL imagick 3)

Imagick::annotateImage — Додає текстовий коментар до зображення

### Опис

```methodsynopsis
public Imagick::annotateImage(    ImagickDraw $draw_settings,    float $x,    float $y,    float $angle,    string $text): bool
```

Додає текстовий коментар до зображення.

### Список параметрів

`draw_settings`

Об'єкт ImagickDraw з налаштуванням тексту

`x`

Горизонтальне зміщення у пікселях зліва від тексту

`y`

Вертикальне зміщення у пікселях до базового тексту

`angle`

Кут під яким виводиться текст. Позитивне значення: напрямок від верхнього лівого кута до правого нижнього кута. Негативне значення: від нижнього лівого кута до верхнього правого кута.

`text`

Рядок з текстом

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::annotateImage()****

Додавання тексту до порожнього зображення

```php
<?php
/* Создаём объекты */
$image = new Imagick();
$draw = new ImagickDraw();
$pixel = new ImagickPixel( 'gray' );

/* Новое изображение */
$image->newImage(800, 75, $pixel);

/* Чёрный текст */
$draw->setFillColor('black');

/* Настройки шрифта */
$draw->setFont('Bookman-DemiItalic');
$draw->setFontSize( 30 );

/* Создаём текст */
$image->annotateImage($draw, 10, 45, 0, 'The quick brown fox jumps over the lazy dog');

/* Устанавливаем формат изображения */
$image->setImageFormat('png');

/* Выводим изображение с заголовками */
header('Content-type: image/png');
echo $image;

?>
```

### Дивіться також

-   [ImagickDraw::annotation()](imagickdraw.annotation.md) - Малює текст на картинці
-   [ImagickDraw::setFont()](imagickdraw.setfont.md) - Встановлює вказаний шрифт для використання під час анотування текстом
