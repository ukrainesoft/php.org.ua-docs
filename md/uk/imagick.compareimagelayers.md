Повертає максимальну область, що обмежує між зображеннями

-   [« Imagick::compareImageChannels](imagick.compareimagechannels.html)
    
-   [Imagick::compareImages »](imagick.compareimages.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає максимальну область, що обмежує між зображеннями
    

# Imagick::compareImageLayers

(PECL imagick 2, PECL imagick 3)

Imagick::compareImageLayers — Повертає максимальну обмежувальну область між зображеннями

### Опис

```methodsynopsis
public Imagick::compareImageLayers(int $method): Imagick
```

Порівнює кожне зображення з наступним у послідовності і повертає максимальну область, що обмежує будь-яких виявлених відмінностей пікселів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`method`

Одна з [констант метода слоя](imagick.constants.html#imagick.constants.layermethod)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::compareImageLayers()****

Порівняння шарів зображення

```php
<?php
/* создание новый объект imagick */
$im = new Imagick("test.gif");

/* оптимизирование слои изображения */
$result = $im->compareImageLayers(imagick::LAYERMETHOD_COALESCE);

/* работа с $result */
?>
```

### Дивіться також

-   [Imagick::optimizeImageLayers()](imagick.optimizeimagelayers.html) - Видаляє повторювані частини зображень для оптимізації
-   [Imagick::writeImages()](imagick.writeimages.html) - Записує зображення або послідовність зображень
-   [Imagick::writeImage()](imagick.writeimage.html) - Записує зображення за вказаним ім'ям файлу