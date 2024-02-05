---
navigation:
  - function.imagecreatefromxbm.md: « imagecreatefromxbm
  - function.imagecreatetruecolor.md: imagecreatetruecolor »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromxpm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromxpm

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromxpm — Створює нове зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromxpm(string $filename): GdImage|false
```

**imagecreatefromxpm()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до зображення XPM.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Создание изображения, используя**imagecreatefromxpm()\*\*\*\*

```php
<?php
// Проверка наличия XPM поддержки
if(!(imagetypes() & IMG_XPM))
{
    die('Поддержка xpm не найдена!');
}

// Создание изображения
$xpm = imagecreatefromxpm('./example.xpm');

// Различные операции с изображением

// PHP не поддерживает запись xpm изображений
// поэтому мы сохраним изображение, как
// jpeg файл со 100% качеством
imagejpeg($xpm, './example.jpg', 100);
imagedestroy($xpm);
?>
```
