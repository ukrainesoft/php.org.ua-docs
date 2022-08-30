Копіює частину зображення з накладенням у градаціях сірого

-   [« imagecopymerge](function.imagecopymerge.md)
    
-   [imagecopyresampled »](function.imagecopyresampled.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Копіює частину зображення з накладенням у градаціях сірого
    

# imagecopymergegray

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagecopymerge gray — Копіює частину зображення з накладенням у градаціях сірого

### Опис

```methodsynopsis
imagecopymergegray(    GdImage $dst_image,    GdImage $src_image,    int $dst_x,    int $dst_y,    int $src_x,    int $src_y,    int $src_width,    int $src_height,    int $pct): bool
```

Копіює частину `src_image` і поміщає скопійоване на `dst_image`, починаючи з координат `src_x` `src_y` із шириною `src_width` та заввишки `src_height`. Скопійована частина міститься на координати `dst_x` і `dst_y`

Функція працює аналогічно [imagecopymerge()](function.imagecopymerge.md) за винятком того, що при накладенні вона зберігає насиченість кольору вихідного зображення шляхом перетворення кольорів пікселів кінцевого зображення в сірому градації перед копіюванням.

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

Результуюче зображення `src_image` буде перетворено на зображення в градаціях сірого відповідно до значення параметра `pct`. 0 означає відсутність кольорів крім сірого, 100 – без змін. Коли `pct` = 100 поведінка функції ідентична [imagecopy()](function.imagecopy.md) для палітрових зображень, незважаючи на те, що в цій функції реалізована прозорість для truecolor-зображень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dst_image` і `src_image` тепер чекають на екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecopymergegray()****

```php
<?php
// Создание изображений
$dest = imagecreatefromgif('php.gif');
$src = imagecreatefromgif('php.gif');

// Копирование и наложение - Серый = 20%
imagecopymergegray($dest, $src, 10, 10, 0, 0, 100, 47, 20);

// Вывод и освобождение памяти
header('Content-Type: image/gif');
imagegif($dest);

imagedestroy($dest);
imagedestroy($src);
?>
```