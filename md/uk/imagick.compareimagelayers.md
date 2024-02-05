---
navigation:
  - imagick.compareimagechannels.md: '« Imagick::compareImageChannels'
  - imagick.compareimages.md: 'Imagick::compareImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::compareImageLayers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::compareImageLayers

(PECL imagick 2, PECL imagick 3)

Imagick::compareImageLayers — Повертає максимальну обмежувальну область між зображеннями

### Опис

```methodsynopsis
public Imagick::compareImageLayers(int $method): Imagick
```

Порівнює кожне зображення з наступним у послідовності і повертає максимальну область, що обмежує будь-яких виявлених відмінностей пікселів. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`method`

Одна из[констант методу шару](imagick.constants.md#imagick.constants.layermethod)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::compareImageLayers()\*\*\*\*

Порівняння шарів зображення

```php
<?php
/* создание новый объект imagick */
$im = new Imagick("test.gif");

/* оптимизирование слои изображения */
$result = $im->compareImageLayers(imagick::LAYERMETHOD_COALESCE);

/* работа с $result */
?>
```

### Дивіться також

-   [Imagick::optimizeImageLayers()](imagick.optimizeimagelayers.md) \- Видаляє повторювані частини зображень для оптимізації
-   [Imagick::writeImages()](imagick.writeimages.md) \- Записує зображення або послідовність зображень
-   [Imagick::writeImage()](imagick.writeimage.md) \- Записує зображення за вказаним ім'ям файлу
