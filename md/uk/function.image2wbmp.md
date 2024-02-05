---
navigation:
  - function.image-type-to-mime-type.md: « image\_type\_to\_mime\_type
  - function.imageaffine.md: imageaffine »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: image2wbmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# image2wbmp

(PHP 4 >= 4.0.5, PHP 5, PHP 7)

image2wbmp — Виводить зображення у браузер або пише у файл

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
image2wbmp(resource $image, string $filename = ?, int $foreground = ?): bool
```

**image2wbmp()** виводить або зберігає WBMP версію заданого зображення `image`

### Список параметрів

`image`

Ресурс зображення, який повертається однією з функцій створення зображення, наприклад [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`filename`

Шлях збереження файла. Якщо не встановлено, вихідні дані зображення будуть виведені безпосередньо у вихідний потік.

`foreground`

Ви можете встановити колір переднього плану за допомогою цього параметра, встановивши ідентифікатор, отриманий за допомогою [imagecolorallocate()](function.imagecolorallocate.md). Колір переднього плану за промовчанням чорний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### Приклади

**Пример #1 Пример использования**image2wbmp()\*\*\*\*

```php
<?php
$file = 'php.png';
$image = imagecreatefrompng($file);

header('Content-Type: ' . image_type_to_mime_type(IMAGETYPE_WBMP));
image2wbmp($image); // вывод потока
imagedestroy($image);
?>
```

### Дивіться також

-   [imagewbmp()](function.imagewbmp.md) \- Виводить зображення у браузер або пише у файл
