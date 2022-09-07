---
navigation:
  - function.imagecreatefromgd.md: « imagecreatefromgd
  - function.imagecreatefromjpeg.md: imagecreatefromjpeg »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreatefromgif
---
# imagecreatefromgif

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreatefromgif — Створює нове зображення з файлу чи URL

### Опис

```methodsynopsis
imagecreatefromgif(string $filename): GdImage|false
```

**imagecreatefromgif()** повертає об'єкт зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Застереження**

При читанні анімованих файлів GIF в пам'ять повертається вказівник на ресурс зображення тільки для першого кадру. Розмір зображення не обов'язково відповідає тому, що поверне функція [getimagesize()](function.getimagesize.md)

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була включена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.md). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Список параметрів

`filename`

Шлях до GIF картинки.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад обробки помилки під час завантаження GIF**

```php
<?php
function LoadGif($imgname)
{
    /* Пытаемся открыть */
    $im = @imagecreatefromgif($imgname);

    /* Если не удалось */
    if(!$im)
    {
        /* Создаём пустое изображение */
        $im = imagecreatetruecolor (150, 30);
        $bgc = imagecolorallocate ($im, 255, 255, 255);
        $tc = imagecolorallocate ($im, 0, 0, 0);

        imagefilledrectangle ($im, 0, 0, 150, 30, $bgc);

        /* Выводим сообщение об ошибке */
        imagestring ($im, 1, 5, 5, 'Ошибка загрузки ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/gif');

$img = LoadGif('bogus.image');

imagegif($img);
imagedestroy($img);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Приклад обробки помилки під час завантаження GIF](images/21009b70229598c6a80eef8b45bf282b-imagecreatefromgif.gif)
