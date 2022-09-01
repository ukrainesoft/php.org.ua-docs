---
navigation:
  - function.imagecreatefromavif.md: « imagecreatefromavif
  - function.imagecreatefromgd2.md: imagecreatefromgd2 »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefrombmp
---
# imagecreatefrombmp

(PHP 7> = 7.2.0, PHP 8)

imagecreatefrombmp — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefrombmp(string $filename): GdImage|false
```

**imagecreatefrombmp()** повертає ідентифікатор зображення, що представляє зображення, одержане з переданого імені файлу.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до BMP-зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Конвертування BMP-зображення в PNG-зображення, використовуючи **imagecreatefrombmp()****

```php
<?php
// Загрузить BMP-файл
$im = imagecreatefrombmp('./example.bmp');

// Преобразовать в PNG-файл с настройками по умолчанию
imagepng($im, './example.png');
imagedestroy($im);
?>
```
