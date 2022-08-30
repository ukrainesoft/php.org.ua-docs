Об'єднує набір зображень

-   [« Imagick::annotateImage](imagick.annotateimage.html)
    
-   [Imagick::autoLevelImage »](imagick.autolevelimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Об'єднує набір зображень
    

# Imagick::appendImages

(PECL imagick 2, PECL imagick 3)

Imagick::appendImages — Об'єднує набір зображень

### Опис

```methodsynopsis
public Imagick::appendImages(bool $stack): Imagick
```

Поєднує набір зображень в одне велике зображення.

### Список параметрів

`stack`

Чи варто складати зображення вертикально. За замовчуванням (або якщо зазначено **`false`**) зображення складаються зліва направо. Якщо `stack` встановлений в \*\*`true`\*\*то зображення складаються зверху вниз.

### Значення, що повертаються

У разі успішного виконання повертає екземпляр Imagick.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::appendImages()****

```php
<?php

/* Создаём новый объект imagick */
$im = new Imagick();

/* создаём красное, зелёное и синее изображения */
$im->newImage(100, 50, "red");
$im->newImage(100, 50, "green");
$im->newImage(100, 50, "blue");

/* Соединяем все изображения в одно */
$im->resetIterator();
$combined = $im->appendImages(true);

/* Выводим изображение */
$combined->setImageFormat("png");
header("Content-Type: image/png");
echo $combined;
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад висновку: Imagick::appendImages()](images/c0d23d2d6769e53e24a1b3136c064577-floodfillpaint_intermediate.png)