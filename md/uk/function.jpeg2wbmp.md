Конвертує зображення з формату JPEG у WBMP

-   [« iptcparse](function.iptcparse.html)
    
-   [png2wbmp »](function.png2wbmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Конвертує зображення з формату JPEG у WBMP
    

# jpeg2wbmp

(PHP 4> = 4.0.5, PHP 5, PHP 7)

jpeg2wbmp — Перетворення зображення з формату JPEG на WBMP

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
jpeg2wbmp(    string $jpegname,    string $wbmpname,    int $dest_height,    int $dest_width,    int $threshold): bool
```

Конвертує JPEG-файл у WBMP.

### Список параметрів

`jpegname`

Шлях до JPEG-файлу.

`wbmpname`

Шлях для розміщення WBMP-файлу.

`dest_height`

Висота WBMP-зображення.

`dest_width`

Ширина WBMP зображення.

`threshold`

Порогове значення від 0 до 8 (включно).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### Приклади

**Приклад #1 Приклад використання **jpeg2wbmp()****

```php
<?php
// Путь к исходному jpeg-изображению
$path = './test.jpg';

// Получаем размеры изображения
$image = getimagesize($path);

// Конвертируем изображение
jpeg2wbmp($path, './test.wbmp', $image[1], $image[0], 5);
?>
```

### Дивіться також

-   [png2wbmp()](function.png2wbmp.html) - Перетворення PNG файлу на WBMP