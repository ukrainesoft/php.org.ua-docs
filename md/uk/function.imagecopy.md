Копіювання частини зображення

-   [« imageconvolution](function.imageconvolution.html)
    
-   [imagecopymerge »](function.imagecopymerge.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Копіювання частини зображення
    

# imagecopy

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecopy — Копіювання частини зображення

### Опис

```methodsynopsis
imagecopy(    GdImage $dst_image,    GdImage $src_image,    int $dst_x,    int $dst_y,    int $src_x,    int $src_y,    int $src_width,    int $src_height): bool
```

Копіює частину `src_image` в `dst_image`починаючи з координат x, y `src_x` `src_y` із шириною `src_width` та заввишки `src_h`. Скопійована частина міститься на координати `dst_x` і `dst_y`

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

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | `dst_image` і `src_image` тепер чекають на екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Обрізання логотипу PHP.net**

```php
<?php
// Создание изображений
$src = imagecreatefromgif('php.gif');
$dest = imagecreatetruecolor(80, 40);

// Копирование
imagecopy($dest, $src, 0, 0, 20, 13, 80, 40);

// Вывод и освобождение памяти
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Обрізання логотипу PHP.net](images/21009b70229598c6a80eef8b45bf282b-imagecopy.gif)

### Дивіться також

-   [imagecrop()](function.imagecrop.html) - Обрізати зображення до заданого прямокутника