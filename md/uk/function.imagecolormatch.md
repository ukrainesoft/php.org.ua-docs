---
navigation:
  - function.imagecolorexactalpha.md: « imagecolorexactalpha
  - function.imagecolorresolve.md: imagecolorresolve »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolormatch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolormatch

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

imagecolormatch — Робить кольори палітрової версії зображення більш відповідними truecolor версії

### Опис

```methodsynopsis
imagecolormatch(GdImage $image1, GdImage $image2): bool
```

Робить кольори палітрової версії зображення більш відповідними truecolor версії.

### Список параметрів

`image1`

Об'єкт truecolor-зображення.

`image2`

Об'єкт палітрового зображення, що має той самий розмір, що і `image1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image1`и`image2` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagecolormatch()\*\*\*\*

```php
<?php
// создание изображений
$im1 = imagecreatefrompng('./gdlogo.png');
$im2 = imagecreate(imagesx($im1), imagesy($im1));

// Добавим несколько цветов в $im2
$colors   = Array();
$colors[] = imagecolorallocate($im2, 255, 36, 74);
$colors[] = imagecolorallocate($im2, 40, 0, 240);
$colors[] = imagecolorallocate($im2, 82, 100, 255);
$colors[] = imagecolorallocate($im2, 84, 63, 44);

// Зададим соответствия этих цветов цветам truecolor изображения
imagecolormatch($im1, $im2);

// освободим память
imagedestroy($im1);
imagedestroy($im2);
?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
