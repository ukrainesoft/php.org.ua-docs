---
navigation:
  - function.imagetypes.md: « imagetypes
  - function.imagewebp.md: imagewebp »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagewbmp
---
# imagewbmp

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

imagewbmp — Виводить зображення до браузера або пише у файл

### Опис

```methodsynopsis
imagewbmp(GdImage $image, resource|string|null $file = null, ?int $foreground_color = null): bool
```

**imagewbmp()** виводить або зберігає у форматі WBMP задане зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

`foreground_color`

Можна встановити колір верхнього шару. Колір задається ідентифікатором, створеним функцією [imagecolorallocate()](function.imagecolorallocate.md). За промовчанням колір чорний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |
|  | `foreground_color` тепер допускає значення null. |

### Приклади

**Приклад #1 Висновок WBMP зображення**

```php
<?php
// создание пустого изображения и добавление текста
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая текстовая строка', $text_color);

// Тип содержимого, в данном случае image/vnd.wap.wbmp
// Подсказка: смотрите image_type_to_mime_type()
header('Content-Type: image/vnd.wap.wbmp');

// Вывод изображения
imagewbmp($im);

// Освобождение памяти
imagedestroy($im);
?>
```

**Приклад #2 Збереження WBMP зображення**

```php
<?php
// создание пустого изображения и добавление текста
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая текстовая строка', $text_color);

// Сохранение изображения
imagewbmp($im, 'simpletext.wbmp');

// Освобождение памяти
imagedestroy($im);
?>
```

**Приклад #3 Виведення зображення зі зміненим верхнім шаром**

```php
<?php
// создание пустого изображения и добавление текста
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая текстовая строка', $text_color);

// Тип содержимого, в данном случае image/vnd.wap.wbmp
// Подсказка: смотрите image_type_to_mime_type()
header('Content-Type: image/vnd.wap.wbmp');

// замена цвета
$foreground_color = imagecolorallocate($im, 255, 0, 0);

imagewbmp($im, NULL, $foreground_color);

// Освобождение памяти
imagedestroy($im);
?>
```

### Дивіться також

-   [image2wbmp()](function.image2wbmp.md) - Виводить зображення у браузер або пише у файл
-   [imagepng()](function.imagepng.md) - Виведення PNG зображення у браузер або файл
-   [imagegif()](function.imagegif.md) - Виводить зображення у браузер або пише у файл
-   [imagejpeg()](function.imagejpeg.md) - Виводить зображення у браузер або пише у файл
-   [imagetypes()](function.imagetypes.md) - Повертає список типів зображень, які підтримує PHP збірка
