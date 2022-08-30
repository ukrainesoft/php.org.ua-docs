Робить кольори палітрової версії зображення більш відповідними truecolor версії

-   [« imagecolorexactalpha](function.imagecolorexactalpha.html)
    
-   [imagecolorresolve »](function.imagecolorresolve.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Робить кольори палітрової версії зображення більш відповідними truecolor версії
    

# imagecolormatch

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

imagecolormatch — Робить кольори палітрової версії зображення більш відповідними truecolor версії

### Опис

```methodsynopsis
imagecolormatch(GdImage $image1, GdImage $image2): bool
```

Робить кольори палітрової версії зображення більш відповідними truecolor версії.

### Список параметрів

`image1`

Об'єкт truecolor-зображення.

`image2`

Об'єкт палітрового зображення, що має той самий розмір, що і `image1`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                           |
|--------|--------------------------------------------------------------------------------------------------------------------|
|        | `image1` і `image2` тепер чекають на екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolormatch()****

```php
<?php
// создание изображений
$im1 = imagecreatefrompng('./gdlogo.png');
$im2 = imagecreate(imagesx($im1), imagesy($im1));

// Добавим несколько цветов в $im2
$colors   = Array();
$colors[] = imagecolorallocate($im2, 255, 36, 74);
$colors[] = imagecolorallocate($im2, 40, 0, 240);
$colors[] = imagecolorallocate($im2, 82, 100, 255);
$colors[] = imagecolorallocate($im2, 84, 63, 44);

// Зададим соответствия этих цветов цветам truecolor изображения
imagecolormatch($im1, $im2);

// освободим память
imagedestroy($im1);
imagedestroy($im2);
?>
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення