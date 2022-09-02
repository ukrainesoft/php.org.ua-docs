---
navigation:
  - function.imagegd.md: « imagegd
  - function.imagegetinterpolation.md: imagegetinterpolation »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegetclip
---
# imagegetclip

(PHP 7> = 7.2.0, PHP 8)

imagegetclip — Отримати прямокутник, що відсікає

### Опис

```methodsynopsis
imagegetclip(GdImage $image): array
```

**imagegetclip()** повертає поточний прямокутник, що відсікає, тобто. область, за межами якої не відображатимуться пікселі.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Функція повертає індексований масив з координатами прямокутником, що відсікає, який має наступні записи:

-   x-координата верхнього лівого кута
-   y-координата верхнього лівого кута
-   x-координата нижнього правого кута
-   y-координата нижнього правого кута

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagegetclip()****

Встановлення та витяг відсікаючого прямокутника.

```php
<?php
$im = imagecreate(100, 100);
imagesetclip($im, 10,10, 89,89);
print_r(imagegetclip($im));
```

Результат виконання цього прикладу:

```
Array
(
    [0] => 10
    [1] => 10
    [2] => 89
    [3] => 89
)
```

### Дивіться також

-   [imagesetclip()](function.imagesetclip.md) - Встановіть прямокутник обмеження
