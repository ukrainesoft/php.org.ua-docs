---
navigation:
  - function.imagewebp.md: « imagewebp
  - function.iptcembed.md: iptcembed »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagexbm
---
# imagexbm

(PHP 5, PHP 7, PHP 8)

imagexbm — Виведення XBM зображення до браузера або файлу

### Опис

```methodsynopsis
imagexbm(GdImage $image, ?string $filename, ?int $foreground_color = null): bool
```

Виведення або збереження у форматі XBM зображення `image`

> **Зауваження** **imagexbm()** не використовує доповнення, тому ширина зображення повинна бути кратна 8. Це обмеження не накладається з версій PHP 7.0.9.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`filename`

Шлях, яким зберігати файл, заданий як рядок (string) Якщо встановлено, чи одно **`null`**, буде здійснено пряме виведення необробленого потоку зображення.

`filename` (без розширення .xbm) також використовується як ідентифікатор C XBM, при цьому символи, що не є у поточній локалі цифрами або літерами, замінюються на підкреслення. Якщо `filename` заданий як **`null`** `image` буде використано для створення ідентифікатора C.

`foreground_color`

Можна встановити колір верхнього шару. Колір визначається ідентифікатором створеним функцією [imagecolorallocate()](function.imagecolorallocate.md). За промовчанням колір чорний. Всі інші кольори інтерпретуються як кольори підкладки (background).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |
|  | `foreground_color` тепер допускає значення null. |
|  | Четвертий параметр, який не використовувався, було видалено. |

### Приклади

**Приклад #1 Збереження файлу XBM**

```php
<?php
// Создание пустого изображения и добавление текста
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая текстовая строка', $text_color);

// Сохранение изображения
imagexbm($im, 'simpletext.xbm');

// Освобождение памяти
imagedestroy($im);
?>
```

**Приклад #2 Збереження файлу XBM з відмінним кольором верхнього шару**

```php
<?php
// Создание пустого изображения и добавление текста
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая текстовая строка', $text_color);

// Изменение цвета
$foreground_color = imagecolorallocate($im, 255, 0, 0);

// Сохранение изображения
imagexbm($im, NULL, $foreground_color);

// Освобождение памяти
imagedestroy($im);
?>
```

### Примітки
