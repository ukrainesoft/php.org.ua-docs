---
navigation:
  - function.imagecolorresolve.md: « imagecolorresolve
  - function.imagecolorset.md: imagecolorset »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorresolvealpha
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorresolvealpha

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

imagecolorresolvealpha — Отримує ідентифікатор конкретного кольору та альфа компонента або його найближчий аналог

### Опис

```methodsynopsis
imagecolorresolvealpha(    GdImage $image,    int $red,    int $green,    int $blue,    int $alpha): int
```

Ця функція обов'язково поверне ідентифікатор кольору для вибраного кольору або найближчу можливу його альтернативу.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

`alpha`

Значение в диапазоне от до`127`. . означає непрозорість, `127` означає абсолютну прозорість.

Параметри кольору можуть бути цілими в діапазоні від 0 до 255, або шістнадцятковими в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Повертає індекс кольору.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagecoloresolvealpha()**для получения цветов из изображения**

```php
<?php
// Загрузка изображения
$im = imagecreatefromgif('phplogo.gif');

// Получение ближайших цветов
$colors = array();
$colors[] = imagecolorresolvealpha($im, 255, 255, 255, 0);
$colors[] = imagecolorresolvealpha($im, 0, 0, 200, 127);

// Вывод
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

-   [imagecolorclosestalpha()](function.imagecolorclosestalpha.md) \- Отримання індексу кольору найближчого до заданого з урахуванням прозорості
