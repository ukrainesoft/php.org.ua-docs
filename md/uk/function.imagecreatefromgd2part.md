---
navigation:
  - function.imagecreatefromgd2.md: « imagecreatefromgd2
  - function.imagecreatefromgd.md: imagecreatefromgd »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgd2part
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromgd2part

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd2part — Створення нового зображення на основі GD2 файлу або URL

### Опис

```methodsynopsis
imagecreatefromgd2part(    string $filename,    int $x,    int $y,    int $width,    int $height): GdImage|false
```

Створення нового зображення на основі GD2 файлу або URL.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

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

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagecreatefromgd2part()\*\*\*\*

```php
<?php
// Для этого примера нам сначала потребуется узнать размер изображения
$image = getimagesize('./test.gd2');

// Создание изображения
$im = imagecreatefromgd2part('./test.gd2', 4, 4, ($image[0] / 2) - 6, ($image[1] / 2) - 6);

// Добавим рельеф на изображение
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_EMBOSS);
}

// сохранение изображения
imagegd2($im, './test_emboss.gd2');
imagedestroy($im);
?>
```

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами зображень libgd. Вони повинні розглядатися як *застарілі* і повинні використовуватися тільки з метою розробки та тестування.
