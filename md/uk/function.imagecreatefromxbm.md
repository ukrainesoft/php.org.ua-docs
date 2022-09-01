---
navigation:
  - function.imagecreatefromwebp.md: « imagecreatefromwebp
  - function.imagecreatefromxpm.md: imagecreatefromxpm »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromxbm
---
# imagecreatefromxbm

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromxbm — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromxbm(string $filename): GdImage|false
```

**imagecreatefromxbm()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до зображення XBM.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Перетворення XBM зображення на png, використовуючи **imagecreatefromxbm()****

```php
<?php
// загрузка xbm файла
$xbm = imagecreatefromxbm('./example.xbm');

// Преобразование в png файл
imagepng($xbm, './example.png');
imagedestroy($xbm);
?>
```
