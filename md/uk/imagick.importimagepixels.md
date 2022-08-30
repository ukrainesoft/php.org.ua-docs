Імпортує пікселі зображення

-   [« Imagick::implodeImage](imagick.implodeimage.html)
    
-   [Imagick::inverseFourierTransformImage »](imagick.inversefouriertransformimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Імпортує пікселі зображення
    

# Imagick::importImagePixels

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::importImagePixels — Імпортує пікселі зображення

### Опис

```methodsynopsis
public Imagick::importImagePixels(    int $x,    int $y,    int $width,    int $height,    string $map,    int $storage,    array $pixels): bool
```

Імпортує пікселі з масиву до зображення . `map` зазвичай "RGB". Цей метод накладає такі обмеження на параметри: кількість пікселів у масиві має відповідати `width` з `height` кількість пікселів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`x`

Положення зображення по осі X.

`y`

Положення зображення по осі Y.

`width`

Ширина зображення.

`height`

Висота зображення.

`map`

Карта упорядкування пікселів у вигляді рядка. Це може бути, наприклад, `RGB`. Значення може бути будь-якою комбінацією або порядком: R = червоний, G = зелений, B = синій, A = альфа (0 - прозорий), O = непрозорий (0 - непрозорий), C = блакитний, Y = жовтий, M = пурпуровий, K = чорний, I = інтенсивність (для відтінків сірого), P = заповнювач.

`storage`

Спосіб зберігання пікселів. Дивіться список [констант пікселів](imagick.constants.html#imagick.constants.pixel)

`pixels`

Масив пікселів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::importImagePixels()****

```php
<?php

/* Создание массива пикселей. 2000 пикселей на цветную полосу */
$count = 2000 * 3;

$pixels =
   array_merge(array_pad(array(), $count, 0),
               array_pad(array(), $count, 255),
               array_pad(array(), $count, 0),
               array_pad(array(), $count, 255),
               array_pad(array(), $count, 0));

/* Ширина и высота. Площадь - это количество пикселей, разделённое на три.
Три происходит от "RGB", три значения на пиксель. */
$width = $height = pow((count($pixels) / 3), 0.5);

/* Создание пустого изображения */
$im = new Imagick();
$im->newImage($width, $height, 'gray');

/* Импорт пикселей в изображение.
   width * height * strlen("RGB") должно соответствовать count($pixels) */
$im->importImagePixels(0, 0, $width, $height, "RGB", Imagick::PIXEL_CHAR, $pixels);

/* Вывод изображения */
$im->setImageFormat('jpg');
header("Content-Type: image/jpg");
echo $im;

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад використання Imagick::importImagePixels()](images/c0d23d2d6769e53e24a1b3136c064577-importimagepixels.jpg)