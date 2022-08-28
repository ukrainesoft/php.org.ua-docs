Виводить зображення у браузер або пише у файл

-   [« image\_type\_to\_mime\_type](function.image-type-to-mime-type.html)
    
-   [imageaffine »](function.imageaffine.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Виводить зображення у браузер або пише у файл
    

# image2wbmp

(PHP 4> = 4.0.5, PHP 5, PHP 7)

image2wbmp — Виводить зображення у браузер або пише у файл

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
image2wbmp(resource $image, string $filename = ?, int $foreground = ?): bool
```

**image2wbmp()** виводить або зберігає WBMP версію заданого зображення `image`

### Список параметрів

`image`

Ресурс зображення, який повертається однією з функцій створення зображення, наприклад [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`filename`

Шлях збереження файла. Якщо не встановлено, вихідні дані зображення будуть виведені безпосередньо у вихідний потік.

`foreground`

Ви можете встановити колір переднього плану за допомогою цього параметра, встановивши ідентифікатор, отриманий за допомогою [imagecolorallocate()](function.imagecolorallocate.html). Колір переднього плану за промовчанням чорний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### Приклади

**Приклад #1 Приклад використання **image2wbmp()****

```php
<?php
$file = 'php.png';
$image = imagecreatefrompng($file);

header('Content-Type: ' . image_type_to_mime_type(IMAGETYPE_WBMP));
image2wbmp($image); // вывод потока
imagedestroy($image);
?>
```

### Дивіться також

-   [imagewbmp()](function.imagewbmp.html) - Виводить зображення до браузера або пише у файл