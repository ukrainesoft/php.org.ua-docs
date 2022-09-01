---
navigation:
  - function.imagescale.md: « imagescale
  - function.imagesetclip.md: imagesetclip »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesetbrush
---
# imagesetbrush

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagesetbrush — Встановлення зображення (пензля), за допомогою якого будуть малюватись лінії

### Опис

```methodsynopsis
imagesetbrush(GdImage $image, GdImage $brush): bool
```

**imagesetbrush()** задає зображення, яке використовуватиметься функціями для малювання ліній (такими як [imageline()](function.imageline.md) і [imagepolygon()](function.imagepolygon.md)) при використанні кольорів **`IMG_COLOR_BRUSHED`** або **`IMG_COLOR_STYLEDBRUSHED`**

**Застереження**

Додаткові дії після завершення роботи з пензлем не потрібні, проте якщо зображення пензля знищено, не можна користуватися квітами **`IMG_COLOR_BRUSHED`** або **`IMG_COLOR_STYLEDBRUSHED`**, доки не буде встановлено нове зображення пензля!

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`brush`

Об'єкт зображення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` і `brush` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesetbrush()****

```php
<?php
// Загрузка минилоготипа php
$php = imagecreatefrompng('./php.png');

// Создание основного изображения 100x100
$im = imagecreatetruecolor(100, 100);

// Заливка фона белым цветом
$white = imagecolorallocate($im, 255, 255, 255);
imagefilledrectangle($im, 0, 0, 299, 99, $white);

// Установка кисти
imagesetbrush($im, $php);

// Рисование линии из изображений кисти
imageline($im, 50, 50, 50, 60, IMG_COLOR_BRUSHED);

// Вывод и очистка памяти
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
imagedestroy($php);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagesetbrush()](images/21009b70229598c6a80eef8b45bf282b-imagesetbrush.png)
