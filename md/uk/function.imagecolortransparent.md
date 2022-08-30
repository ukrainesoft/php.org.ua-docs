Визначає колір як прозорий

-   [« imagecolorstotal](function.imagecolorstotal.md)
    
-   [imageconvolution »](function.imageconvolution.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Визначає колір як прозорий
    

# зображенняcolortransparent

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolortransparent — Визначає колір як прозорий

### Опис

```methodsynopsis
imagecolortransparent(GdImage $image, ?int $color = null): int
```

Отримує або встановлює прозорість кольору у заданому зображенні `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає ідентифікатор нового (або поточного, якщо нічого не змінилося) кольору. Якщо аргумент `color` заданий як **`null`** і у зображенні немає прозорих кольорів, функція поверне `-1`

### список змін

| Версия | Описание                                                                                       |
|--------|------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |
|        | `color` тепер допускає значення null.                                                          |

### Приклади

**Приклад #1 Приклад використання **imagecolortransparent()****

```php
<?php
// Создадим изображение размером 55x30
$im = imagecreatetruecolor(55, 30);
$red = imagecolorallocate($im, 255, 0, 0);
$black = imagecolorallocate($im, 0, 0, 0);

// Сделаем фон прозрачным
imagecolortransparent($im, $black);

// Нарисуем красный прямоугольник
imagefilledrectangle($im, 4, 4, 50, 25, $red);

// Сохраним изображение
imagepng($im, './imagecolortransparent.png');
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagecolortransparent()](images/21009b70229598c6a80eef8b45bf282b-imagecolortransparent.png)

### Примітки

> **Зауваження**
> 
> Прозорість копіюється лише функцією [imagecopymerge()](function.imagecopymerge.md) і для truecolor-зображень. У разі використання функції [imagecopy()](function.imagecopy.md) або палітрового зображення значення альфа компонента не копіюється.

> **Зауваження**
> 
> Прозорий колір є властивістю зображення, прозорість не є властивістю кольору. Якщо ви задали колір як прозорий, деякі області зображення цього кольору намальовані раніше стануть прозорими.