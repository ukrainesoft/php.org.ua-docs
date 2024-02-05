---
navigation:
  - function.getimagesizefromstring.md: « getimagesizefromstring
  - function.image-type-to-mime-type.md: image\_type\_to\_mime\_type »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: image\_type\_to\_extension
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# image\_type\_to\_extension

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

image\_type\_to\_extension — отримання розширення файлу для типу зображення

### Опис

```methodsynopsis
image_type_to_extension(int $image_type, bool $include_dot = true): string|false
```

Повертає розширення файлу для заданої `IMAGETYPE_XXX` константи.

### Список параметрів

`image_type`

Одна из констант`IMAGETYPE_XXX`

`include_dot`

Додавати крапку до розширення чи ні. За замовчуванням **`true`**

### Значення, що повертаються

Строка с расширением файла, соответствующим типу изображения или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**image\_type\_to\_extension()\*\*\*\*

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

> **Зауваження** :
> 
> Ця функція не потребує бібліотеки GD.
