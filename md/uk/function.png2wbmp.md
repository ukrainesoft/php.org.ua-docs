Перетворення PNG файлу на WBMP

-   [« jpeg2wbmp](function.jpeg2wbmp.html)
    
-   [GdImage »](class.gdimage.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Перетворення PNG файлу на WBMP
    

# png2wbmp

(PHP 4> = 4.0.5, PHP 5, PHP 7)

png2wbmp — Перетворення PNG файлу на WBMP

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
png2wbmp(    string $pngname,    string $wbmpname,    int $dest_height,    int $dest_width,    int $threshold): bool
```

Перетворює PNG файл на WBMP.

### Список параметрів

`pngname`

Шлях до файлу PNG.

`wbmpname`

Шлях до результуючого WBMP файлу.

`dest_height`

Висота результуючого зображення.

`dest_width`

Ширина результуючого зображення.

`threshold`

Обмеження від 0 до 8 (включно).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### Приклади

**Приклад #1 Приклад використання **png2wbmp()****

```php
<?php
// Путь к png
$path = './test.png';

// Получение размеров изображений
$image = getimagesize($path);

// Преобразование
png2wbmp($path, './test.wbmp', $image[1], $image[0], 7);
?>
```

### Дивіться також

-   [jpeg2wbmp()](function.jpeg2wbmp.html) - Конвертує зображення з формату JPEG у WBMP