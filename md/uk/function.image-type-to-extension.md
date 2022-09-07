---
navigation:
  - function.getimagesizefromstring.md: « getimagesizefromstring
  - function.image-type-to-mime-type.md: imagetypeтоmimetype »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagetypeтоextension
---
# imagetypeтоextension

(PHP 5> = 5.2.0, PHP 7, PHP 8)

imagetypeтоextension — отримання розширення файлу для типу зображення

### Опис

```methodsynopsis
image_type_to_extension(int $image_type, bool $include_dot = true): string|false
```

Повертає розширення файлу для заданої `IMAGETYPE_XXX` константи.

### Список параметрів

`image_type`

Одна з констант `IMAGETYPE_XXX`

`include_dot`

Додавати крапку до розширення чи ні. За замовчуванням **`true`**

### Значення, що повертаються

Рядок з розширенням файлу, що відповідає типу зображення або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **imagetypeтоextension()****

```php
<?php
// Создание изображения
$im = imagecreatetruecolor(100, 100);

// Сохранение изображения
imagepng($im, './test' . image_type_to_extension(IMAGETYPE_PNG));
imagedestroy($im);
?>
```

### Примітки

> **Зауваження**
> 
> Ця функція не потребує бібліотеки GD.
