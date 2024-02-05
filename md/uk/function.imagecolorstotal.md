---
navigation:
  - function.imagecolorsforindex.md: « imagecolorsforindex
  - function.imagecolortransparent.md: imagecolortransparent »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorstotal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorstotal

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorstotal — Визначення кількості кольорів на панелі зображення.

### Опис

```methodsynopsis
imagecolorstotal(GdImage $image): int
```

Повертає кількість кольорів на панелі зображення.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає кількість кольорів на панелі зображення або 0 для truecolor-зображень.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Получение количества цветов в изображении, используя**imagecolorstotal()\*\*\*\*

```php
<?php
// Создание изображения
$im = imagecreatefromgif('php.gif');

echo 'Всего цветов в изображении: ' . imagecolorstotal($im);

// Освобождение памяти
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Всего цветов в изображении: 128
```

### Дивіться також

-   [imagecolorat()](function.imagecolorat.md) \- Отримання індексу кольору пікселя
-   [imagecolorsforindex()](function.imagecolorsforindex.md) \- Отримання кольорів, що відповідають індексу
-   [imageistruecolor()](function.imageistruecolor.md) \- Визначає, чи є зображення повнокольоровим
