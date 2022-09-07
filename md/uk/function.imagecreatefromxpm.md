---
navigation:
  - function.imagecreatefromxbm.md: « imagecreatefromxbm
  - function.imagecreatetruecolor.md: imagecreatetruecolor »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromxpm
---
# imagecreatefromxpm

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromxpm — Створює нове зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromxpm(string $filename): GdImage|false
```

**imagecreatefromxpm()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до зображення XPM.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Створення зображення за допомогою **imagecreatefromxpm()****

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
