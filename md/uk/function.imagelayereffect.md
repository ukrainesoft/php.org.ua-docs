---
navigation:
  - function.imagejpeg.md: « imagejpeg
  - function.imageline.md: imageline »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagelayereffect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagelayereffect

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

imagelayereffect — Встановлення прапора альфа пару для використання ефектів накладання зображень

### Опис

```methodsynopsis
imagelayereffect(GdImage $image, int $effect): bool
```

Встановлення прапора альфа пару для використання ефектів накладання зображень.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`effect`

Одна з наступних констант:

**`IMG_EFFECT_REPLACE`**

Використовувати заміну пікселів (аналогічно передачі \*\*`true`\*\*в[imagealphablending()](function.imagealphablending.md)) .

**`IMG_EFFECT_ALPHABLEND`**

Використовувати звичайне сполучення кольорів (аналогічно передачі \*\*`false`\*\*в[imagealphablending()](function.imagealphablending.md)) .

**`IMG_EFFECT_NORMAL`**

Те саме, що і **`IMG_EFFECT_ALPHABLEND`**

**`IMG_EFFECT_OVERLAY`**

В результаті накладання картинки з цим ефектом чорні і білі пікселі фону зображення залишаться так само чорними і білими, а сірі змінить колір на колір пікселя зображення, що накладається.

**`IMG_EFFECT_MULTIPLY`**

Оверлєї з множником ефекту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 7.2.0 | Додана **`IMG_EFFECT_MULTIPLY`** (вимагає системну бібліотеку libgd >= 2.1.1 або libgd, що йде в комплекті з PHP). |

### Приклади

**Пример #1 Пример использования**imagelayereffect()\*\*\*\*

```php
<?php
// Задание изображения
$im = imagecreatetruecolor(100, 100);

// Установка фона
imagefilledrectangle($im, 0, 0, 100, 100, imagecolorallocate($im, 220, 220, 220));

// Применение флага альфа сопряжения - overlay
imagelayereffect($im, IMG_EFFECT_OVERLAY);

// Рисуем два серых эллипса
imagefilledellipse($im, 50, 50, 40, 40, imagecolorallocate($im, 100, 255, 100));
imagefilledellipse($im, 50, 50, 50, 80, imagecolorallocate($im, 100, 100, 255));
imagefilledellipse($im, 50, 50, 80, 50, imagecolorallocate($im, 255, 100, 100));

// Вывод
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagelayereffect()](images/21009b70229598c6a80eef8b45bf282b-imagelayereffect.png)
