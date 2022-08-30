Копіювання палітри з одного зображення до іншого

-   [« imageopenpolygon](function.imageopenpolygon.md)
    
-   [imagepalettetotruecolor »](function.imagepalettetotruecolor.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Копіювання палітри з одного зображення до іншого
    

# imagepalettecopy

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagepalettecopy — Копіювання палітри з одного зображення до іншого

### Опис

```methodsynopsis
imagepalettecopy(GdImage $dst, GdImage $src): void
```

**imagepalettecopy()** копіює палітру кольорів із зображення `src` у зображення `dst`

### Список параметрів

`dst`

Об'єкт результуючого зображення.

`src`

Об'єкт вихідного зображення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание                                                                                                  |
|--------|-----------------------------------------------------------------------------------------------------------|
|        | `dst` і `src` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagepalettecopy()****

```php
<?php
// Создание двух палитровых изображений
$palette1 = imagecreate(100, 100);
$palette2 = imagecreate(100, 100);

// Зелёный фон у первого изображения
$green = imagecolorallocate($palette1, 0, 255, 0);

// Копирование палитры из 1го во 2е изображение
imagepalettecopy($palette2, $palette1);

// Так как палитра скопирована с уже созданным зелёным цветом
// нет нужды использовать imagecolorallocate() дважды
imagefilledrectangle($palette2, 0, 0, 99, 99, $green);

// Вывод изображения в броузер
header('Content-type: image/png');

imagepng($palette2);
imagedestroy($palette1);
imagedestroy($palette2);
?>
```