---
navigation:
  - function.imagecolorclosestalpha.md: « imagecolorclosestalpha
  - function.imagecolordeallocate.md: imagecolordeallocate »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorclosesthwb
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorclosesthwb

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

imagecolorclosesthwb — Отримання індексу кольору, що має заданий тон, білизну та затемнення

### Опис

```methodsynopsis
imagecolorclosesthwb(    GdImage $image,    int $red,    int $green,    int $blue): int
```

Отримання індексу кольору, що має значення тону, білизни та затемнення найбільш близькі до заданого кольору.

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

Повертає цілий індекс кольору, що має значення тону, білизни і затемнення найбільш близькі до заданого кольору.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagecolorclosesthwb()\*\*\*\*

```php
<?php
$im = imagecreatefromgif('php.gif');

echo 'HWB: ' . imagecolorclosesthwb($im, 116, 115, 152);

imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

```
HWB: 33
```

### Дивіться також

-   [imagecolorclosest()](function.imagecolorclosest.md) \- Отримання індексу кольору найближчого до заданого
