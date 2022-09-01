---
navigation:
  - function.imagecolorresolvealpha.md: « imagecolorresolvealpha
  - function.imagecolorsforindex.md: imagecolorsforindex »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorset
---
# imagecolorset

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorset — Встановлення набору кольорів для заданого індексу панелі

### Опис

```methodsynopsis
imagecolorset(    GdImage $image,    int $color,    int $red,    int $green,    int $blue,    int $alpha = 0): ?bool
```

Функція встановлює відповідність індексу на панелі заданого кольору. Це корисно для створення ефекту подібного до заливання кольором без здійснення заливки.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`color`

Індекс на панелі.

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

`alpha`

Значення компонента альфа.

### Значення, що повертаються

Функція повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolorset()****

```php
<?php
// Создание изображения размером 300x100
$im = imagecreate(300, 100);

// Установка красного цвета фона
imagecolorallocate($im, 255, 0, 0);

// Получение индекса цвета фона
$bg = imagecolorat($im, 0, 0);

// Установка синего цвета фона
imagecolorset($im, $bg, 0, 0, 255);

// Вывод изображения в браузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Дивіться також

-   [imagecolorat()](function.imagecolorat.md) - Отримання індексу кольору пікселя
