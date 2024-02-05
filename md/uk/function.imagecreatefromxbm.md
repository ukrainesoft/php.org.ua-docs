---
navigation:
  - function.imagecreatefromwebp.md: « imagecreatefromwebp
  - function.imagecreatefromxpm.md: imagecreatefromxpm »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromxbm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreatefromxbm

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromxbm — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromxbm(string $filename): GdImage|false
```

**imagecreatefromxbm()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

### Список параметрів

`filename`

Шлях до зображення XBM.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Преобразование XBM изображения в png, используя**imagecreatefromxbm()\*\*\*\*

```php
<?php
// загрузка xbm файла
$xbm = imagecreatefromxbm('./example.xbm');

// Преобразование в png файл
imagepng($xbm, './example.png');
imagedestroy($xbm);
?>
```
