---
navigation:
  - function.imageaffinematrixget.md: « imageaffinematrixget
  - function.imageantialias.md: imageantialias »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagealphablending
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagealphablending

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagealphablending — Встановлення режиму сполучення кольорів зображення

### Опис

```methodsynopsis
imagealphablending(GdImage $image, bool $enable): bool
```

**imagealphablending()** дозволяє використовувати режим сполучення кольорів для truecolor-зображень при малюванні. У режимі сполучення альфа компонент кольору, який передається всім функціям малювання, на зразок [imagesetpixel()](function.imagesetpixel.md), визначає те, наскільки сильно колір нижнього шару буде просочуватися через зображення, що накладається. В результаті, gd автоматично сполучає існуючий колір у кожній точці з кольором зображеного поверх зображення та зберігає результат сполучення у зображенні. Піксели, що зазнали поєднання, не мають властивості прозорості. У режимі без сполучення колір малювання поверх піксела буквально копіюється разом зі своїм альфа компонентом, замінюючи піксел у вихідному зображенні. Режим сполучення недоступний для малювання на палітрових зображеннях.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`enable`

Увімкнути режим сполучення чи ні. Включено (**`true`**) за замовчуванням для truecolor-зображень, для всіх інших за замовчуванням вимкнено (**`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagealphablending()\*\*\*\*

```php
<?php
// Создание изображения
$im = imagecreatetruecolor(100, 100);

// Включение режима сопряжения цветов
imagealphablending($im, true);

// Рисуем прямоугольник
imagefilledrectangle($im, 30, 30, 70, 70, imagecolorallocate($im, 255, 0, 0));

// Вывод
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```
