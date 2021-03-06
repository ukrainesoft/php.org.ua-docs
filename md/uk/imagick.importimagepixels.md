- [« Imagick::implodeImage](imagick.implodeimage.md)
- [Imagick::inverseFourierTransformImage »](imagick.inversefouriertransformimage.md)

- [PHP Manual](index.md)
- [Imagick](class.imagick.md)
- Імпортує пікселі зображення

# Imagick::importImagePixels

(PECL imagick 2 \>= 2.3.0, PECL imagick 3)

Imagick::importImagePixels — Імпортує пікселі зображення

### Опис

public **Imagick::importImagePixels**(
int `$x`,
int `$y`,
int `$width`,
int `$height`,
string `$map`,
int `$storage`,
array `$pixels`
): bool

Імпортує пікселі з масиву зображення. `map` зазвичай "RGB". Цей
метод накладає такі обмеження на параметри: кількість
пікселів у масиві має відповідати `width` x `height` кількості
пікселів. Цей метод доступний, якщо Imagick був скомпільований з версією
ImageMagick 6.4.5 або старше.

### Список параметрів

`x`
Положення зображення на осі X.

`y`
Положення зображення по осі Y.

`width`
Ширина зображення.

`height`
Висота зображення.

`map`
Карта впорядкування пікселів у вигляді рядка. Це може бути, наприклад,
`RGB`. Значення може бути будь-якою комбінацією або порядком: R = червоний,
G = зелений, B = синій, A = альфа (0 – прозорий), O = непрозорий
(0 - непрозорий), C = блакитний, Y = жовтий, M = пурпурний, K = чорний,
I = інтенсивність (для відтінків сірого), P = заповнювач.

`storage`
Спосіб зберігання пікселів. Дивіться список [констант пікселів](imagick.constants.md#imagick.constants.pixel).

`pixels`
Масив пікселів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::importImagePixels()****

`<?php/* Створення масиву пікселів. 2000 пикселей на цветную полосу */$count = 2000 * 3;$pixels =   array_merge(array_pad(array(), $count, 0),               array_pad(array(), $count, 255),               array_pad(array(), $ count, 0),               array_pad(array(), $count, 255),                  array_pad(array; і) Площа - це кількість пікселей, розділене на три.Три відбувається від "RGB", три значення на піксель. */$width = $height = pow((count($pixels) / 3), 0.5);/* Створення пустого зображення */$im = new Imagick();$im->newImage($width, $ 'gray');/* Імпорт пікселів в зображення. width * height * strlen("RGB") повинно відповідати count($pixels) */$im->importImagePixels(0, 0, $width, $height, "RGB", Imagick::PIXEL_CH Висновок зображення */$im->setImageFormat('jpg');header("Content-Type: image/jpg");echo $im;?> `

Результатом виконання цього прикладу буде щось подібне:

![Приклад використання
Imagick::importImagePixels()](images/c0d23d2d6769e53e24a1b3136c064577-importimagepixels.jpg)
