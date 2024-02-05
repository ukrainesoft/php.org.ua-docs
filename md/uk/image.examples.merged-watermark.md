---
navigation:
  - image.examples-watermark.md: « Додавання водяних знаків на зображення за допомогою альфа-каналів
  - ref.image.md: Функції GD та функції для роботи із зображеннями »
  - index.md: PHP Manual
  - image.examples.md: Приклади
title: >-
  Использование[imagecopymerge()](function.imagecopymerge.md) створити
  напівпрозорий водяний знак
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Использование[imagecopymerge()](function.imagecopymerge.md) створити напівпрозорий водяний знак

**Пример #1 Использование[imagecopymerge()](function.imagecopymerge.md) створити напівпрозорий водяний знак**

```php
<?php
// Загрузка штампа и фото, для которого применяется водяной знак (называется штамп или печать)
$im = imagecreatefromjpeg('photo.jpeg');

// Сначала создаём наше изображение штампа вручную с помощью GD
$stamp = imagecreatetruecolor(100, 70);
imagefilledrectangle($stamp, 0, 0, 99, 69, 0x0000FF);
imagefilledrectangle($stamp, 9, 9, 90, 60, 0xFFFFFF);
imagestring($stamp, 5, 20, 20, 'libGD', 0x0000FF);
imagestring($stamp, 3, 20, 40, '(c) 2007-9', 0x0000FF);

// Установка полей для штампа и получение высоты/ширины штампа
$marge_right = 10;
$marge_bottom = 10;
$sx = imagesx($stamp);
$sy = imagesy($stamp);

// Слияние штампа с фотографией. Прозрачность 50%
imagecopymerge($im, $stamp, imagesx($im) - $sx - $marge_right, imagesy($im) - $sy - $marge_bottom, 0, 0, imagesx($stamp), imagesy($stamp), 50);

// Сохранение фотографии в файл и освобождение памяти
imagepng($im, 'photo_stamp.png');
imagedestroy($im);

?>
```

![Використання imagecopymerge() для створення напівпрозорого водяного знаку](images/21009b70229598c6a80eef8b45bf282b-watermark-merged.png)

У цьому прикладі використовується [imagecopymerge()](function.imagecopymerge.md) для об'єднання штампу з нашим вихідним зображенням. За допомогою цього ми можемо встановити прозорість нашого штампу - у прикладі ми встановили його на 50% непрозорості (opacity). На практиці це було б корисним для захисту авторських прав, напівпрозорі водяні знаки важко видалити та дозволяють глядачам побачити зображення.
