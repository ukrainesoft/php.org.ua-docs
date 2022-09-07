---
navigation:
  - function.imagecreatefromwbmp.md: « imagecreatefromwbmp
  - function.imagecreatefromxbm.md: imagecreatefromxbm »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromwebp
---
# imagecreatefromwebp

(PHP 5> = 5.4.0, PHP 7, PHP 8)

imagecreatefromwebp — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromwebp(string $filename): GdImage|false
```

**imagecreatefromwebp()** повертає ідентифікатор зображення, що представляє зображення, одержане з переданого імені файлу. Зауважте, що анімовані файли WebP не читаються.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до WebP-зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Конвертування WebP-зображення до jpeg-зображення, використовуючи **imagecreatefromwebp()****

```php
<?php
// Загрузить WebP-файл
$im = imagecreatefromwebp('./example.webp');

// Сконвертировать его в jpeg-файл со 100%-качеством
imagejpeg($im, './example.jpeg', 100);
imagedestroy($im);
?>
```
