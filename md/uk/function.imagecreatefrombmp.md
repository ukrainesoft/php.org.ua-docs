---
navigation:
  - function.imagecreatefromavif.md: « imagecreatefromavif
  - function.imagecreatefromgd2.md: imagecreatefromgd2 »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefrombmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefrombmp

(PHP 7 >= 7.2.0, PHP 8)

imagecreatefrombmp — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefrombmp(string $filename): GdImage|false
```

**imagecreatefrombmp()** повертає ідентифікатор зображення, що представляє зображення, одержане з переданого імені файлу.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до BMP-зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Конвертирование BMP-изображения в PNG-изображения, используя**imagecreatefrombmp()\*\*\*\*

```php
<?php
// Загрузить BMP-файл
$im = imagecreatefrombmp('./example.bmp');

// Преобразовать в PNG-файл с настройками по умолчанию
imagepng($im, './example.png');
imagedestroy($im);
?>
```
