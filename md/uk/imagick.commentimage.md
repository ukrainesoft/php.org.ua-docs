Додає коментар до вашого зображення

-   [« Imagick::combineImages](imagick.combineimages.md)
    
-   [Imagick::compareImageChannels »](imagick.compareimagechannels.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Додає коментар до вашого зображення
    

# Imagick::commentImage

(PECL imagick 2, PECL imagick 3)

Imagick::commentImage — Додає коментар до вашого зображення

### Опис

```methodsynopsis
public Imagick::commentImage(string $comment): bool
```

Додає коментар до зображення.

### Список параметрів

`comment`

Коментар для додавання

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::commentImage()****

Коментування зображення та отримання коментаря:

```php
<?php

/* Создать новый объект Imagick */
$im = new imagick();

/* Создать пустое изображение */
$im->newImage(100, 100, new ImagickPixel("red"));

/* Добавить комментарий к изображению */
$im->commentImage("Привет, Мир!");

/* Показать комментарий */
echo $im->getImageProperty("comment");

?>
```