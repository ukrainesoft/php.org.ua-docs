Розрив асоціації змінної із кольором для заданого зображення

-   [« imagecolorclosesthwb](function.imagecolorclosesthwb.html)
    
-   [imagecolorexact »](function.imagecolorexact.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Розрив асоціації змінної із кольором для заданого зображення
    

# imagecolordeallocate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolordeallocate — Розрив асоціації змінної із кольором для заданого зображення

### Опис

```methodsynopsis
imagecolordeallocate(GdImage $image, int $color): bool
```

Розриває асоціацію змінної з кольором, яка раніше була створена функціями [imagecolorallocate()](function.imagecolorallocate.html) або [imagecolorallocatealpha()](function.imagecolorallocatealpha.html)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`color`

Ідентифікатор кольору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolordeallocate()****

```php
<?php
$white = imagecolorallocate($im, 255, 255, 255);
imagecolordeallocate($im, $white);
?>
```

### Дивіться також

-   [imagecolorallocate()](function.imagecolorallocate.html) - Створення кольору для зображення
-   [imagecolorallocatealpha()](function.imagecolorallocatealpha.html) - Створення кольору для зображення