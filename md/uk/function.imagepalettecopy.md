---
navigation:
  - function.imageopenpolygon.md: « imageopenpolygon
  - function.imagepalettetotruecolor.md: imagepalettetotruecolor »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagepalettecopy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagepalettecopy

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

imagepalettecopy — Копіювання палітри з одного зображення до іншого

### Опис

```methodsynopsis
imagepalettecopy(GdImage $dst, GdImage $src): void
```

\*\*imagepalettecopy()\*\*копирует палитру цветов из изображения`src`в изображение`dst`

### Список параметрів

`dst`

Об'єкт результуючого зображення.

`src`

Об'єкт вихідного зображення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `dst`и`src` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання** imagepalettecopy()\*\*\*\*

```php
<?php
// Создание двух палитровых изображений
$palette1 = imagecreate(100, 100);
$palette2 = imagecreate(100, 100);

// Зелёный фон у первого изображения
$green = imagecolorallocate($palette1, 0, 255, 0);

// Копирование палитры из 1го во 2е изображение
imagepalettecopy($palette2, $palette1);

// Так как палитра скопирована с уже созданным зелёным цветом
// нет нужды использовать imagecolorallocate() дважды
imagefilledrectangle($palette2, 0, 0, 99, 99, $green);

// Вывод изображения в броузер
header('Content-type: image/png');

imagepng($palette2);
imagedestroy($palette1);
imagedestroy($palette2);
?>
```
