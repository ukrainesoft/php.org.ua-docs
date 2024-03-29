---
navigation:
  - function.imagecolorat.md: « imagecolorat
  - function.imagecolorclosestalpha.md: imagecolorclosestalpha »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorclosest
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorclosest

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorclosest — Отримання індексу кольору найближчого до заданого

### Опис

```methodsynopsis
imagecolorclosest(    GdImage $image,    int $red,    int $green,    int $blue): int
```

Повертає індекс кольору на панелі зображення, "найближчого" до заданого значення RGB.

"Відстань" між кольорами на палітрі розраховується геометрично, начебто RGB значення були представлені у вигляді точок у тривимірному просторі.

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

Параметри кольору можуть бути цілими в діапазоні від 0 до 255, або шістнадцятковими в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Повертає індекс кольору на панелі зображення, найближчого до заданого.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Пошук набору кольорів зображення**

```php
<?php
// Создание изображения и преобразование его в палитровое
$im = imagecreatefrompng('figures/imagecolorclosest.png');
imagetruecolortopalette($im, false, 255);

// Цвета для поиска (RGB)
$colors = array(
    array(254, 145, 154),
    array(153, 145, 188),
    array(153, 90, 145),
    array(255, 137, 92)
);

// Проход по каждому цвету и поиск ближайшего к нему в палитре.
// Возврат номера по порядку, RGB искомого цвета и найденное RGB соответствие
foreach($colors as $id => $rgb)
{
    $result = imagecolorclosest($im, $rgb[0], $rgb[1], $rgb[2]);
    $result = imagecolorsforindex($im, $result);
    $result = "({$result['red']}, {$result['green']}, {$result['blue']})";

    echo "#$id: Поиск ($rgb[0], $rgb[1], $rgb[2]); Ближайшее сходство: $result.\n";
}

imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

```
#0: Поиск (254, 145, 154); Ближайшее сходство: (252, 150, 148).
#1: Поиск (153, 145, 188); Ближайшее сходство: (148, 150, 196).
#2: Поиск (153, 90, 145); Ближайшее сходство: (148, 90, 156).
#3: Поиск (255, 137, 92); Ближайшее сходство: (252, 150, 92).
```

### Дивіться також

-   [imagecolorexact()](function.imagecolorexact.md) \- Отримання індексу заданого кольору
-   [imagecolorclosestalpha()](function.imagecolorclosestalpha.md) \- Отримання індексу кольору найближчого до заданого з урахуванням прозорості
-   [imagecolorclosesthwb()](function.imagecolorclosesthwb.md) \- Отримання індексу кольору, що має заданий тон, білизну та затемнення
