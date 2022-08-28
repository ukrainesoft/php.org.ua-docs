Встановлення прапора альфа пару для використання ефектів накладання зображень

-   [« imagejpeg](function.imagejpeg.html)
    
-   [imageline »](function.imageline.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Встановлення прапора альфа пару для використання ефектів накладання зображень
    

# imagelayereffect

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

imagelayereffect — Встановлення прапора альфа пару для використання ефектів накладання зображень

### Опис

```methodsynopsis
imagelayereffect(GdImage $image, int $effect): bool
```

Встановлення прапора альфа пару для використання ефектів накладання зображень.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`effect`

Одна з наступних констант:

**`IMG_EFFECT_REPLACE`**

Використовувати заміну пікселів (аналогічно передачі **`true`** в [imagealphablending()](function.imagealphablending.html)

**`IMG_EFFECT_ALPHABLEND`**

Використовувати звичайне сполучення кольорів (аналогічно передачі **`false`** в [imagealphablending()](function.imagealphablending.html)

**`IMG_EFFECT_NORMAL`**

Те саме, що і **`IMG_EFFECT_ALPHABLEND`**

**`IMG_EFFECT_OVERLAY`**

В результаті накладання картинки з цим ефектом чорні та білі пікселі фону зображення залишаться так само чорними та білими, а сірі змінять колір на колір пікселя зображення, що накладається.

**`IMG_EFFECT_MULTIPLY`**

Оверлєї з множником ефекту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource).                   |
|        | Додана **`IMG_EFFECT_MULTIPLY`** (вимагає системну бібліотеку libgd >= 2.1.1 або libgd, що йде в комплекті з PHP). |

### Приклади

**Приклад #1 Приклад використання **imagelayereffect()****

```php
<?php
// Задание изображения
$im = imagecreatetruecolor(100, 100);

// Установка фона
imagefilledrectangle($im, 0, 0, 100, 100, imagecolorallocate($im, 220, 220, 220));

// Применение флага альфа сопряжения - overlay
imagelayereffect($im, IMG_EFFECT_OVERLAY);

// Рисуем два серых эллипса
imagefilledellipse($im, 50, 50, 40, 40, imagecolorallocate($im, 100, 255, 100));
imagefilledellipse($im, 50, 50, 50, 80, imagecolorallocate($im, 100, 100, 255));
imagefilledellipse($im, 50, 50, 80, 50, imagecolorallocate($im, 255, 100, 100));

// Вывод
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagelayereffect()](images/21009b70229598c6a80eef8b45bf282b-imagelayereffect.png)