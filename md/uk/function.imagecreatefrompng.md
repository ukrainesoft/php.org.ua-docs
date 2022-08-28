Створює нове зображення з файлу чи URL

-   [« imagecreatefromjpeg](function.imagecreatefromjpeg.html)
    
-   [imagecreatefromstring »](function.imagecreatefromstring.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Створює нове зображення з файлу чи URL
    

# imagecreatefrompng

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreatefrompng — Створення нового зображення з файлу або URL

### Опис

```methodsynopsis
imagecreatefrompng(string $filename): GdImage|false
```

**imagecreatefrompng()** повертає ідентифікатор зображення, що представляє зображення, отримане з файлу із заданим ім'ям.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.html). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Поддерживаемые протоколы и обёртки](wrappers.html)

### Список параметрів

`filename`

Шлях до зображення PNG.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад обробки помилки під час завантаження PNG**

```php
<?php
function LoadPNG($imgname)
{
    /* Пытаемся открыть */
    $im = @imagecreatefrompng($imgname);

    /* Если не удалось */
    if(!$im)
    {
        /* Создаём пустое изображение */
        $im  = imagecreatetruecolor(150, 30);
        $bgc = imagecolorallocate($im, 255, 255, 255);
        $tc  = imagecolorallocate($im, 0, 0, 0);

        imagefilledrectangle($im, 0, 0, 150, 30, $bgc);

        /* Выводим сообщение об ошибке */
        imagestring($im, 1, 5, 5, 'Ошибка загрузки ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/png');

$img = LoadPNG('bogus.image');

imagepng($img);
imagedestroy($img);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад використання imagecreatefrompng()](images/21009b70229598c6a80eef8b45bf282b-imagecreatefrompng.png)