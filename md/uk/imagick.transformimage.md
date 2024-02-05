---
navigation:
  - imagick.tostring.md: '« Imagick::\_\_function toString() { [native code] }'
  - imagick.transformimagecolorspace.md: 'Imagick::transformImageColorspace »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::transformImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::transformImage

(PECL imagick 2, PECL imagick 3)

Imagick::transformImage — Зручний метод налаштування розміру кадрування та геометрії зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::transformImage(string $crop, string $geometry): Imagick
```

Зручний метод налаштування розміру кадрування та геометрії зображення з рядків. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`crop`

Рядок геометрії обрізки. Геометрія визначає підобласть зображення для обрізання.

`geometry`

Рядок геометрії зображення. Геометрія визначає остаточний розмір зображення.

### Значення, що повертаються

Повертає об'єкт Imagick, який містить перетворене зображення.

### Приклади

**Приклад #1 Приклад використання** Imagick::transformImage()\*\* :\*\*

У прикладі створюється чорне зображення розміром 100×100.

```php
<?php
$image = new Imagick();
$image->newImage(300, 200, "black");
$new_image = $image->transformImage("100x100", "100x100");
$new_image->writeImage('test_out.jpg');
?>
```

### Дивіться також

-   [Imagick::cropImage()](imagick.cropimage.md) \- Витягує область зображення
-   [Imagick::resizeImage()](imagick.resizeimage.md) \- Масштабує зображення
-   [Imagick::thumbnailImage()](imagick.thumbnailimage.md) \- Змінює розмір зображення
