---
navigation:
  - function.imagesetbrush.md: « imagesetbrush
  - function.imagesetinterpolation.md: imagesetinterpolation »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesetclip
---
# imagesetclip

(PHP 7> = 7.2.0, PHP 8)

imagesetclip — Встановіть прямокутник обмеження

### Опис

```methodsynopsis
imagesetclip(    GdImage $image,    int $x1,    int $y1,    int $x2,    int $y2): bool
```

**imagesetclip()** ставить поточний прямокутник обмеження, тобто. область, за межами якої не відображатимуться пікселі.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x1`

Координата x верхнього лівого кута.

`y1`

Координата по y верхнього лівого кута.

`x2`

Координата x нижнього лівого кута.

`y2`

Координата з y нижнього правого кута.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [imagegetclip()](function.imagegetclip.md) - Отримати прямокутник, що відсікає
