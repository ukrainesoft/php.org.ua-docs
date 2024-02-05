---
navigation:
  - function.imagesetthickness.md: « imagesetthickness
  - function.imagestring.md: imagestring »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesettile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagesettile

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagesettile — Встановлення зображення, яке буде використано як елемент мозаїчної заливки

### Опис

```methodsynopsis
imagesettile(GdImage $image, GdImage $tile): bool
```

**imagesettile()** задає зображення, яке буде використано як елемент мозаїчної заливки такими функціями, як [imagefill()](function.imagefill.md) і [imagefilledpolygon()](function.imagefilledpolygon.md)при использовании специального цвета\*\*`IMG_COLOR_TILED`\*\*

Це зображення використовується для замощення області зображення копіями. Може використовувати *будь-яке* GD зображення. А якщо встановити прозорий колір для цього зображення функцією [imagecolortransparent()](function.imagecolortransparent.md), деякі частини зображення нижче будуть просвічувати через створену мозаїку.

**Застереження**

Додаткові дії після завершення роботи з мозаїчним елементом не потрібні, однак якщо це зображення буде видалено (або дозволити PHP видалити його), не можна використовувати колір \*\*`IMG_COLOR_TILED`\*\*до тех пор, пока не будет задано новое изображение!

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`tile`

Об'єкт зображення для використання в мозаїці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image`и`tile` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagesettile()\*\*\*\*

```php
<?php
// Загрузка внешнего изображения
$zend = imagecreatefromgif('./zend.gif');

// Создание изображения 200x200
$im = imagecreatetruecolor(200, 200);

// Установка мозаичного элемента
imagesettile($im, $zend);

// Заливка
imagefilledrectangle($im, 0, 0, 199, 199, IMG_COLOR_TILED);

// Вывод картинки в броузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
imagedestroy($zend);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagesettile()](images/21009b70229598c6a80eef8b45bf282b-imagesettile.png)
