Визначення кількості кольорів на панелі зображення

-   [« imagecolorsforindex](function.imagecolorsforindex.html)
    
-   [imagecolortransparent »](function.imagecolortransparent.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Визначення кількості кольорів на панелі зображення
    

# imagecolorstotal

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorstotal — Визначення кількості кольорів на панелі зображення.

### Опис

```methodsynopsis
imagecolorstotal(GdImage $image): int
```

Повертає кількість кольорів на панелі зображення.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає кількість кольорів на панелі зображення або 0 для truecolor-зображень.

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Отримання кількості кольорів у зображенні за допомогою **imagecolorstotal()****

```php
<?php
// Создание изображения
$im = imagecreatefromgif('php.gif');

echo 'Всего цветов в изображении: ' . imagecolorstotal($im);

// Освобождение памяти
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Всего цветов в изображении: 128
```

### Дивіться також

-   [imagecolorat()](function.imagecolorat.html) - Отримання індексу кольору пікселя
-   [imagecolorsforindex()](function.imagecolorsforindex.html) - Отримання кольорів, що відповідають індексу
-   [imageistruecolor()](function.imageistruecolor.html) - Визначає, чи є зображення повнокольоровим