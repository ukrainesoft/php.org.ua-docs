---
navigation:
  - function.imagecolormatch.md: « imagecolormatch
  - function.imagecolorresolvealpha.md: imagecolorresolvealpha »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorresolve
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorresolve

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorresolve — Отримує ідентифікатор конкретного кольору або його найближчий аналог

### Опис

```methodsynopsis
imagecolorresolve(    GdImage $image,    int $red,    int $green,    int $blue): int
```

Ця функція обов'язково поверне ідентифікатор кольору для вибраного кольору або найближчу можливу його альтернативу.

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

Повертає колірний ідентифікатор.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Использование**imagecoloresolve()**для получения цветов из изображения.**

```php
<?php
// загрузить изображение
$im = imagecreatefromgif('phplogo.gif');

// получить ближайшие цвета на изображении
$colors = array();
$colors[] = imagecolorresolve($im, 255, 255, 255);
$colors[] = imagecolorresolve($im, 0, 0, 200);

// вывод
print_r($colors);

imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => 89
    [1] => 85
)
```

### Дивіться також

-   [imagecolorclosest()](function.imagecolorclosest.md) \- Отримання індексу кольору найближчого до заданого
