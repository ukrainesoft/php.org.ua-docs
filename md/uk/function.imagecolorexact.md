---
navigation:
  - function.imagecolordeallocate.md: « imagecolordeallocate
  - function.imagecolorexactalpha.md: imagecolorexactalpha »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorexact
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorexact

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorexact — Отримання індексу заданого кольору

### Опис

```methodsynopsis
imagecolorexact(    GdImage $image,    int $red,    int $green,    int $blue): int
```

Повертає індекс для заданого кольору на панелі зображення.

Якщо зображення було створено з файлу, розпізнаються лише кольори, що використовуються у зображенні. Кольори, які використовуються лише на палітрі, не розпізнано.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

### Значення, що повертаються

Повертає індекс для заданого кольору на панелі зображення або -1, якщо такого кольору на панелі немає.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Отримання кольорів GD логотипу**

```php
<?php
// создание изображения
$im = imagecreatefrompng('./gdlogo.png');

$colors   = Array();
$colors[] = imagecolorexact($im, 255, 0, 0);
$colors[] = imagecolorexact($im, 0, 0, 0);
$colors[] = imagecolorexact($im, 255, 255, 255);
$colors[] = imagecolorexact($im, 100, 255, 52);

print_r($colors);

// освобождение памяти
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => 16711680
    [1] => 0
    [2] => 16777215
    [3] => 6618932
)
```

### Дивіться також

-   [imagecolorclosest()](function.imagecolorclosest.md) \- Отримання індексу кольору найближчого до заданого
