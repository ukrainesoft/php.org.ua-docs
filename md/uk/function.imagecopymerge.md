Копіює частину зображення з накладенням

-   [« imagecopy](function.imagecopy.html)
    
-   [imagecopymergegray »](function.imagecopymergegray.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Копіює частину зображення з накладенням
    

# imagecopymerge

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagecopymerge — Копіює частину зображення з накладенням

### Опис

```methodsynopsis
imagecopymerge(    GdImage $dst_image,    GdImage $src_image,    int $dst_x,    int $dst_y,    int $src_x,    int $src_y,    int $src_width,    int $src_height,    int $pct): bool
```

Копіює частину `src_image` і поміщає скопійоване на `dst_image`, починаючи з координат `src_x` `src_y` із шириною `src_width` та заввишки `src_height`. Скопійована частина міститься на координати `dst_x` і `dst_y`

### Список параметрів

`dst_image`

Ресурс цільового зображення.

`src_image`

Ресурс вихідного зображення.

`dst_x`

x-координата результуючого зображення.

`dst_y`

y-координата результуючого зображення.

`src_x`

x-координата вихідного зображення.

`src_y`

y-координата вихідного зображення.

`src_width`

Ширина вихідного зображення.

`src_height`

Висота вихідного зображення.

`pct`

Два зображення поєднуються в залежності від параметра `pct`, який може змінюватись від 0 до 100. Коли `pct` = 0, накладення немає. У разі значення 100 ця функція поводиться аналогічно до функції [imagecopy()](function.imagecopy.html) для палітрових зображень, незважаючи на те, що вона підтримує прозорість для truecolor-зображень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                 |
|--------|--------------------------------------------------------------------------------------------------------------------------|
|        | `dst_image` і `src_image` тепер чекають на екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Поєднання двох копій логотипу PHP.net з 75% прозорістю**

```php
<?php
// Создание изображений
$dest = imagecreatefromgif('php.gif');
$src = imagecreatefromgif('php.gif');

// Копирование и наложение
imagecopymerge($dest, $src, 10, 10, 0, 0, 100, 47, 75);

// Вывод и освобождение памяти
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```