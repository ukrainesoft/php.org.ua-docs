---
navigation:
  - function.imagecopyresized.md: « imagecopyresized
  - function.imagecreatefromavif.md: imagecreatefromavif »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecreate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecreate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreate - Створення нового палітрового зображення

### Опис

```methodsynopsis
imagecreate(int $width, int $height): GdImage|false
```

\*\*imagecreate()\*\*возвращает идентификатор изображения, представляющего из себя пустое изображение заданного размера.

Ми рекомендуємо використовувати функцію [imagecreatetruecolor()](function.imagecreatetruecolor.md) замість **imagecreate()**, оскільки вона обробляє зображення з максимально можливою якістю. Якщо потрібно вивести палітру зображення, то [imagetruecolortopalette()](function.imagetruecolortopalette.md) необхідно викликати безпосередньо перед збереженням зображення за допомогою [imagepng()](function.imagepng.md) або [imagegif()](function.imagegif.md)

### Список параметрів

`width`

Ширина зображення.

`height`

Висота зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Створення нового потоку GD зображення та виведення зображення.**

```php
<?php
header("Content-Type: image/png");
$im = @imagecreate(110, 20)
    or die("Невозможно создать поток изображения");
$background_color = imagecolorallocate($im, 0, 0, 0);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  "A Simple Text String", $text_color);
imagepng($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: Створення нового GD потоку зображення та виведення зображення.](images/21009b70229598c6a80eef8b45bf282b-imagecreate.png)

### Дивіться також

-   [imagedestroy()](function.imagedestroy.md) \- Знищення зображення
-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
