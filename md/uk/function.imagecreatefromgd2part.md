---
navigation:
  - function.imagecreatefromgd2.html: « imagecreatefromgd2
  - function.imagecreatefromgd.html: imagecreatefromgd »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgd2part
---
# imagecreatefromgd2part

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd2part — Створення нового зображення на основі GD2 файлу або URL

### Опис

```methodsynopsis
imagecreatefromgd2part(    string $filename,    int $x,    int $y,    int $width,    int $height): GdImage|false
```

Створення нового зображення на основі GD2 файлу або URL.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.html). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.html)

### Список параметрів

`filename`

Шлях до GD2 зображення.

`x`

x-координата точки вихідного зображення.

`y`

y-координата точки вихідного зображення.

`width`

Ширина вихідного зображення.

`height`

Висота вихідного зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecreatefromgd2part()****

```php
<?php
// Для этого примера нам сначала потребуется узнать размер изображения
$image = getimagesize('./test.gd2');

// Создание изображения
$im = imagecreatefromgd2part('./test.gd2', 4, 4, ($image[0] / 2) - 6, ($image[1] / 2) - 6);

// Добавим рельеф на изображение
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_EMBOSS);
}

// сохранение изображения
imagegd2($im, './test_emboss.gd2');
imagedestroy($im);
?>
```

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами зображень libgd. Вони повинні розглядатися як *застарілі* і повинні використовуватися тільки з метою розробки та тестування.
