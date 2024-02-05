---
navigation:
  - function.imagecreatefromwbmp.md: « imagecreatefromwbmp
  - function.imagecreatefromxbm.md: imagecreatefromxbm »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromwebp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromwebp

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

imagecreatefromwebp — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromwebp(string $filename): GdImage|false
```

**imagecreatefromwebp()** повертає ідентифікатор зображення, що представляє зображення, одержане з переданого імені файлу. Зауважте, що анімовані файли WebP не читаються.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до WebP-зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Конвертирование WebP-изображения к jpeg-изображению, используя**imagecreatefromwebp()\*\*\*\*

```php
<?php
// Загрузить WebP-файл
$im = imagecreatefromwebp('./example.webp');

// Сконвертировать его в jpeg-файл со 100%-качеством
imagejpeg($im, './example.jpeg', 100);
imagedestroy($im);
?>
```
