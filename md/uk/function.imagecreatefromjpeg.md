---
navigation:
  - function.imagecreatefromgif.md: « imagecreatefromgif
  - function.imagecreatefrompng.md: imagecreatefrompng »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromjpeg
---
# imagecreatefromjpeg

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreatefromjpeg — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefromjpeg(string $filename): GdImage|false
```

**imagecreatefromjpeg()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до JPEG картинки.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад обробки помилки під час завантаження JPEG**

```php
<?php
function LoadJpeg($imgname)
{
    /* Пытаемся открыть */
    $im = @imagecreatefromjpeg($imgname);

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

header('Content-Type: image/jpeg');

$img = LoadJpeg('bogus.image');

imagejpeg($img);
imagedestroy($img);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок приклад: Приклад обробки помилки під час завантаження JPEG](images/21009b70229598c6a80eef8b45bf282b-imagecreatefromjpeg.jpg)
