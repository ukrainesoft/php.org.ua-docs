---
navigation:
  - function.imagegetclip.md: « imagegetclip
  - function.imagegif.md: imagegif »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegetinterpolation
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagegetinterpolation

(PHP 8)

imagegetinterpolation — Отримує метод інтерполяції

### Опис

```methodsynopsis
imagegetinterpolation(GdImage $image): int
```

Отримує встановлений метод інтерполяції. `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає метод інтерполяції.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Дивіться також

-   [imagesetinterpolation()](function.imagesetinterpolation.md) \- встановлює метод інтерполяції
