---
navigation:
  - function.imagecreatefromtga.md: « imagecreatefromtga
  - function.imagecreatefromwebp.md: imagecreatefromwebp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromwbmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromwbmp

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromwbmp — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromwbmp(string $filename): GdImage|false
```

**imagecreatefromwbmp()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

> **Зауваження**: Зображення WBMP є Wireless Bitmaps, а не Windows Bitmaps. Останні можуть бути завантажені за допомогою [imagecreatefrombmp()](function.imagecreatefrombmp.md)

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до WBMP.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад обробки помилки під час завантаження WBMP**

```php
<?php
function LoadWBMP($imgname)
{
    /* Пытаемся открыть */
    $im = @imagecreatefromwbmp($imgname);

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

header('Content-Type: image/vnd.wap.wbmp');

$img = LoadWBMP('bogus.image');

imagewbmp($img);
imagedestroy($img);
?>
```
