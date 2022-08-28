Отримання висоти зображення

-   [« imagesx](function.imagesx.html)
    
-   [imagetruecolortopalette »](function.imagetruecolortopalette.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Отримання висоти зображення
    

# imagesy

(PHP 4, PHP 5, PHP 7, PHP 8)

imagesy — Отримання висоти зображення

### Опис

```methodsynopsis
imagesy(GdImage $image): int
```

Повертає висоту заданого зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає висоту зображення `image` або **`false`** у разі помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesy()****

```php
<?php

// Создание изображения 300*200
$img = imagecreatetruecolor(300, 200);

echo imagesy($img); // 200

?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення
-   [getimagesize()](function.getimagesize.html) - Отримання розміру зображення
-   [imagesx()](function.imagesx.html) - Отримання ширини зображення