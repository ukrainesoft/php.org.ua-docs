---
navigation:
  - function.imagecolorstotal.md: « imagecolorstotal
  - function.imageconvolution.md: imageconvolution »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolortransparent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolortransparent

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolortransparent — Визначає колір як прозорий

### Опис

```methodsynopsis
imagecolortransparent(GdImage $image, ?int $color = null): int
```

Отримує або встановлює прозорість кольору у заданому зображенні `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає ідентифікатор нового (або поточного, якщо нічого не змінилося) кольору. Якщо аргумент `color`задан как\*\*`null`\*\* і у зображенні немає прозорих кольорів, функція поверне `-1`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | `color` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** imagecolortransparent()\*\*\*\*

```php
<?php
// Создадим изображение размером 55x30
$im = imagecreatetruecolor(55, 30);
$red = imagecolorallocate($im, 255, 0, 0);
$black = imagecolorallocate($im, 0, 0, 0);

// Сделаем фон прозрачным
imagecolortransparent($im, $black);

// Нарисуем красный прямоугольник
imagefilledrectangle($im, 4, 4, 50, 25, $red);

// Сохраним изображение
imagepng($im, './imagecolortransparent.png');
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagecolortransparent()](images/21009b70229598c6a80eef8b45bf282b-imagecolortransparent.png)

### Примітки

> **Зауваження** :
> 
> Прозорість копіюється лише функцією [imagecopymerge()](function.imagecopymerge.md)и для truecolor-изображений. В случае использования функции[imagecopy()](function.imagecopy.md)или палитрового изображения значение альфа компонента не копируется.

> **Зауваження** :
> 
> Прозорий колір є властивістю зображення, прозорість не є властивістю кольору. Якщо ви задали колір як прозорий, деякі області зображення цього кольору намальовані раніше стануть прозорими.
