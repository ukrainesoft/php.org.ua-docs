---
navigation:
  - function.jpeg2wbmp.md: « jpeg2wbmp
  - class.gdimage.md: GdImage »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: png2wbmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# png2wbmp

(PHP 4 >= 4.0.5, PHP 5, PHP 7)

png2wbmp — Перетворює файл PNG на файл WBMP

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### Приклади

**Пример #1 Пример использования**png2wbmp()\*\*\*\*

```php
<?php
// Путь к png
$path = './test.png';

// Получение размеров изображений
$image = getimagesize($path);

// Преобразование
png2wbmp($path, './test.wbmp', $image[1], $image[0], 7);
?>
```

### Дивіться також

-   [jpeg2wbmp()](function.jpeg2wbmp.md) \- Конвертує зображення з формату JPEG у WBMP
