---
navigation:
  - function.imagesetstyle.md: « imagesetstyle
  - function.imagesettile.md: imagesettile »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesetthickness
---
# imagesetthickness

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagesetthickness — Встановлення товщини ліній

### Опис

```methodsynopsis
imagesetthickness(GdImage $image, int $thickness): bool
```

**imagesetthickness()** визначає значення товщини ліній для малювання відрізків, прямокутників, багатокутників, еліпсів і т.п. в `thickness` пікселів.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`thickness`

Товщина пікселів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesetthickness()****

```php
<?php
// Создание изображения 200x100
$im = imagecreatetruecolor(200, 100);
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);

// Установка белого фона
imagefilledrectangle($im, 0, 0, 299, 99, $white);

// Установка толщины линий 5 пикселов
imagesetthickness($im, 5);

// Рисование прямоугольника
imagerectangle($im, 14, 14, 185, 85, $black);

// Вывод изображения в броузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagesetthickness()](images/21009b70229598c6a80eef8b45bf282b-imagesetthickness.png)
