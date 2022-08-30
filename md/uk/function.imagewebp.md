Виведення зображення WebP у браузер або файл

-   [« imagewbmp](function.imagewbmp.html)
    
-   [imagexbm »](function.imagexbm.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Виведення зображення WebP у браузер або файл
    

# imagewebp

(PHP 5> = 5.4.0, PHP 7, PHP 8)

imagewebp — Виведення зображення WebP у браузер або файл

### Опис

```methodsynopsis
imagewebp(GdImage $image, resource|string|null $file = null, int $quality = -1): bool
```

Виведе або збереже WebP-версію цього зображення (`image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

`quality`

`quality` варіюється від 0 (найгірша якість, менший розмір файлу) до 100 (найкраща якість, великий файл).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Збереження WebP-файлу**

```php
<?php
// Создать пустое изображение и добавить текст
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);

imagestring($im, 1, 5, 5,  'WebP with PHP', $text_color);

// Сохранить изображение
imagewebp($im, 'php.webp');

// Освободить память
imagedestroy($im);
?>
```