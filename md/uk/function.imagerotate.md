Поворот зображення із заданим кутом

-   [« imageresolution](function.imageresolution.html)
    
-   [imagesavealpha »](function.imagesavealpha.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Поворот зображення із заданим кутом
    

# imagerotate

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

imagerotate — Повертання зображення із заданим кутом.

### Опис

```methodsynopsis
imagerotate(    GdImage $image,    float $angle,    int $background_color,    bool $ignore_transparent = false): GdImage|false
```

Поворот зображення `image` на заданий кут `angle` у градусах.

Центром повороту є центр зображення. Повертається зображення може відрізнятися розміром від оригіналу.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`angle`

Кут повороту в градусах проти годинникової стрілки.

`background_color`

Колір фон вільної зони після повороту.

`ignore_transparent`

Параметр не використовується.

### Значення, що повертаються

Повертає об'єкт поверненого зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                        |
|--------|---------------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource).                                |
|        | Невикористовуваний `v` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int).                            |

### Приклади

**Приклад #1 Повертання зображення на 180 градусів**

Цей приклад повертає зображення на 180 градусів – верхи вниз.

```php
<?php
// Файл и угол поворота
$filename = 'test.jpg';
$degrees = 180;

// Тип содержимого
header('Content-type: image/jpeg');

// Загрузка изображения
$source = imagecreatefromjpeg($filename);

// Поворот
$rotate = imagerotate($source, $degrees, 0);

// Вывод
imagejpeg($rotate);

// Высвобождение памяти
imagedestroy($source);
imagedestroy($rotate);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад виведе зображення, повернене на 180 градусів.](images/21009b70229598c6a80eef8b45bf282b-imagerotate.jpg)

### Примітки

> **Зауваження**
> 
> Ця функція піддається впливу методу інтерполяції, встановленим функцією [imagesetinterpolation()](function.imagesetinterpolation.html)

### Дивіться також

-   [imagesetinterpolation()](function.imagesetinterpolation.html) - встановлює метод інтерполяції