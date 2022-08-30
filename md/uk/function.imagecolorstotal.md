Визначення кількості кольорів на панелі зображення

-   [« imagecolorsforindex](function.imagecolorsforindex.md)
    
-   [imagecolortransparent »](function.imagecolortransparent.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
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

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає кількість кольорів на панелі зображення або 0 для truecolor-зображень.

### список змін

| Версия | Описание                                                                                       |
|--------|------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

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

-   [imagecolorat()](function.imagecolorat.md) - Отримання індексу кольору пікселя
-   [imagecolorsforindex()](function.imagecolorsforindex.md) - Отримання кольорів, що відповідають індексу
-   [imageistruecolor()](function.imageistruecolor.md) - Визначає, чи є зображення повнокольоровим