Завантаження шрифту

-   [« imageline](function.imageline.md)
    
-   [imageopenpolygon »](function.imageopenpolygon.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Завантаження шрифту
    

# imageloadfont

(PHP 4, PHP 5, PHP 7, PHP 8)

imageloadfont — Завантаження шрифту

### Опис

```methodsynopsis
imageloadfont(string $filename): GdFont|false
```

**imageloadfont()** завантажує певний користувачем шрифт та повертає його ідентифікатор.

### Список параметрів

`filename`

Формат файлу шрифту є двійковим і залежить від архітектури системи. Це означає необхідність генерувати файл шрифту на тому самому процесорі, на якому працює PHP.

**Формат файлу шрифту**

| позиция байта | тип данных C | описание |
| --- | --- | --- |
| байти 0-3 | int | кількість символів у шрифті |
| байти 4-7 | int | значення першого символу у шрифті (часто 32 - пробіл) |
| байти 8-11 | int | ширина пікселя кожного символу |
| байти 12-15 | int | висота пікселя кожного символу |
| байти 16- | char | масив з даними символів, один байт на пікселі в кожному символі. Для всіх к-тьвисоташирина б. |

### Значення, що повертаються

Повертає екземпляр [GdFont](class.gdfont.md) або **`false`** у разі виникнення помилки. Ідентифікатор шрифту, який завжди більше 5 для запобігання конфліктам із вбудованими шрифтами, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [GdFont](class.gdfont.md); раніше поверталося ціле число (int). |

### Приклади

**Приклад #1 Приклад використання **imageloadfont()****

```php
<?php
// Создание нового изображения
$im = imagecreatetruecolor(50, 20);
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);

// Белый фон
imagefilledrectangle($im, 0, 0, 49, 19, $white);

// Загрузка gd шрифта и надпись 'Привет'
$font = imageloadfont('./04b.gdf');
imagestring($im, $font, 0, 0, 'Привет', $black);

// Вывод изображения
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Дивіться також

-   [imagefontwidth()](function.imagefontwidth.md) - Отримання ширини шрифту
-   [imagefontheight()](function.imagefontheight.md) - Отримання висоти шрифту