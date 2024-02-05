---
navigation:
  - function.imagecreatefromjpeg.md: « imagecreatefromjpeg
  - function.imagecreatefromstring.md: imagecreatefromstring »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefrompng
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefrompng

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreatefrompng — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefrompng(string $filename): GdImage|false
```

**imagecreatefrompng()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до зображення PNG.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад обробки помилки під час завантаження PNG**

```php
<?php
function LoadPNG($imgname)
{
    /* Пытаемся открыть */
    $im = @imagecreatefrompng($imgname);

    /* Если не удалось */
    if(!$im)
    {
        /* Создаём пустое изображение */
        $im  = imagecreatetruecolor(150, 30);
        $bgc = imagecolorallocate($im, 255, 255, 255);
        $tc  = imagecolorallocate($im, 0, 0, 0);

        imagefilledrectangle($im, 0, 0, 150, 30, $bgc);

        /* Выводим сообщение об ошибке */
        imagestring($im, 1, 5, 5, 'Ошибка загрузки ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/png');

$img = LoadPNG('bogus.image');

imagepng($img);
imagedestroy($img);
?>
```

Висновок наведеного прикладу буде схожим на:

![Приклад використання imagecreatefrompng()](images/21009b70229598c6a80eef8b45bf282b-imagecreatefrompng.png)
