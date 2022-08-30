Зручний метод налаштування розміру кадрування та геометрії зображення

-   [« Imagick::toString](imagick.tostring.html)
    
-   [Imagick::transformImageColorspace »](imagick.transformimagecolorspace.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Зручний метод налаштування розміру кадрування та геометрії зображення
    

# Imagick::transformImage

(PECL imagick 2, PECL imagick 3)

Imagick::transformImage — Зручний метод налаштування розміру кадрування та геометрії зображення

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::transformImage(string $crop, string $geometry): Imagick
```

Зручний метод налаштування розміру кадрування та геометрії зображення з рядків. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`crop`

Рядок геометрії обрізки. Геометрія визначає підобласть зображення для обрізання.

`geometry`

Рядок геометрії зображення. Геометрія визначає остаточний розмір зображення.

### Значення, що повертаються

Повертає об'єкт Imagick, який містить перетворене зображення.

### Приклади

**Приклад #1 Приклад використання **Imagick::transformImage()****

У прикладі створюється чорне зображення розміром 100×100.

```php
<?php
$image = new Imagick();
$image->newImage(300, 200, "black");
$new_image = $image->transformImage("100x100", "100x100");
$new_image->writeImage('test_out.jpg');
?>
```

### Дивіться також

-   [Imagick::cropImage()](imagick.cropimage.html) - Витягує область зображення
-   [Imagick::resizeImage()](imagick.resizeimage.html) - Масштабує зображення
-   [Imagick::thumbnailImage()](imagick.thumbnailimage.html) - Змінює розмір зображення