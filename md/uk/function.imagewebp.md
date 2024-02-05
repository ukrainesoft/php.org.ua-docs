---
navigation:
  - function.imagewbmp.md: « imagewbmp
  - function.imagexbm.md: imagexbm »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagewebp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagewebp

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

imagewebp — Виведення зображення WebP у браузер або файл

### Опис

```methodsynopsis
imagewebp(GdImage $image, resource|string|null $file = null, int $quality = -1): bool
```

Виведе або збереже WebP-версію цього зображення (`image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

`quality`

`quality` варіюється від 0 (найгірша якість, менший розмір файлу) до 100 (найкраща якість, великий файл).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Збереження WebP-файлу**

```php
<?php
// Создать пустое изображение и добавить текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);

imagestring($im, 1, 5, 5,  'WebP with PHP', $text_color);

// Сохранить изображение
imagewebp($im, 'php.webp');

// Освободить память
imagedestroy($im);
?>
```
