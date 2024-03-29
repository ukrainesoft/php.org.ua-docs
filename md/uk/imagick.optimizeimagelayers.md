---
navigation:
  - imagick.opaquepaintimage.md: '« Imagick::opaquePaintImage'
  - imagick.orderedposterizeimage.md: 'Imagick::orderedPosterizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::optimizeImageLayers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::optimizeImageLayers

(PECL imagick 2, PECL imagick 3)

Imagick::optimizeImageLayers — Видаляє повторювані частини зображень для оптимізації

### Опис

```methodsynopsis
public Imagick::optimizeImageLayers(): bool
```

Порівнює кожне зображення, розташоване у форматі GIF, із попереднім зображенням у послідовності. Виходячи з цього, функція намагається вибрати найменше зображення, що обрізає, для заміни кожного кадру, зберігаючи при цьому результати анімації. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::optimizeImageLayers()\*\*\*\*

Читання, оптимізація та запис зображення у форматі GIF

```php
<?php
/* создание нового объекта imagick */
$im = new Imagick("test.gif");

/* оптимизация слоёв изображения */
$im->optimizeImageLayers();

/* запись изображения обратно */
$im->writeImages("test_optimized.gif", true);
?>
```

### Дивіться також

-   [Imagick::compareImageLayers()](imagick.compareimagelayers.md) \- Повертає максимальну обмежуючу область між зображеннями
-   [Imagick::writeImages()](imagick.writeimages.md) \- Записує зображення або послідовність зображень
-   [Imagick::writeImage()](imagick.writeimage.md) \- Записує зображення за вказаним ім'ям файлу
