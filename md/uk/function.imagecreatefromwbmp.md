---
navigation:
  - function.imagecreatefromtga.md: « imagecreatefromtga
  - function.imagecreatefromwebp.md: imagecreatefromwebp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefrombmp
---
# imagecreatefrombmp

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagecreatefromwbmp — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromwbmp(string $filename): GdImage|false
```

**imagecreatefrombmp()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

> **Зауваження**: Зображення WBMP є Wireless Bitmaps, а не Windows Bitmaps. Останні можуть бути завантажені за допомогою [imagecreatefrombmp()](function.imagecreatefrombmp.md)

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до WBMP.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

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
