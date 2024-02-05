---
navigation:
  - function.imagepalettecopy.md: « imagepalettecopy
  - function.imagepng.md: imagepng »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagepalettetotruecolor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagepalettetotruecolor

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

imagepalettetotruecolor — Перетворює зображення на основі палітри на справжній колір

### Опис

```methodsynopsis
imagepalettetotruecolor(GdImage $image): bool
```

Перетворює зображення на основі палітри, наприклад, створене функцією [imagecreate()](function.imagecreate.md), зображення з істинним кольором (TrueColor), яке, наприклад, створює функція [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає **`true`**, якщо перетворення завершено, або якщо вихідне зображення вже є зображенням справжнього кольору, інакше повертається **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Конвертує будь-який об'єкт зображення на цей колір**

```php
<?php
// Для обратной совместимости
if(!function_exists('imagepalettetotruecolor'))
{
    function imagepalettetotruecolor(&$src)
    {
        if(imageistruecolor($src))
        {
            return(true);
        }

        $dst = imagecreatetruecolor(imagesx($src), imagesy($src));

        imagecopy($dst, $src, 0, 0, 0, 0, imagesx($src), imagesy($src));
        imagedestroy($src);

        $src = $dst;

        return(true);
    }
}

// Анонимная функция-помощник
$typeof = function() use($im)
{
    echo 'typeof($im) = ' . (imageistruecolor($im) ? 'true color' : 'palette'), PHP_EOL;
};

// Создание изображения на основе палитры
$im = imagecreate(100, 100);
$typeof();

// Преобразовать в настоящий цвет
imagepalettetotruecolor($im);
$typeof();

// Освободить память
imagedestroy($im);
?>
```

Результат виконання наведеного прикладу:

```
typeof($im) = palette
typeof($im) = true color
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
-   [imageistruecolor()](function.imageistruecolor.md) \- Визначає, чи є зображення повнокольоровим
