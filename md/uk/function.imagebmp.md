---
navigation:
  - function.imageavif.md: « imageavif
  - function.imagechar.md: imagechar »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagebmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagebmp

(PHP 7 >= 7.2.0, PHP 8)

imagebmp — Вивести BMP-зображення у браузер або файл

### Опис

```methodsynopsis
imagebmp(GdImage $image, resource|string|null $file = null, bool $compressed = true): bool
```

Виводить або зберігає BMP-версію заданого зображення (`image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

> **Зауваження** :
> 
> \*\*`null`\*\*недействителен, если аргумент`compressed` не використовується.

`compressed`

Чи повинен BMP бути стиснутий з кодуванням довжин серій (RLE), чи ні.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | Тип параметра `compressed` тепер логічне значення (bool); раніше був цілим числом (int). |

### Приклади

**Приклад #1 Збереження BMP-файлу**

```php
<?php
// Создайте пустое изображение и добавьте текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);

imagestring($im, 1, 5, 5,  'BMP with PHP', $text_color);

// Сохранить изображение
imagebmp($im, 'php.bmp');

// Освободить память
imagedestroy($im);
?>
```
