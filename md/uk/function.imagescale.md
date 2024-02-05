---
navigation:
  - function.imagesavealpha.md: « imagesavealpha
  - function.imagesetbrush.md: imagesetbrush »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagescale
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagescale

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

imagescale — Масштабувати зображення за заданою шириною та висотою

### Опис

```methodsynopsis
imagescale(    GdImage $image,    int $width,    int $height = -1,    int $mode = IMG_BILINEAR_FIXED): GdImage|false
```

**imagescale()** масштабує зображення, використовуючи заданий алгоритм інтерполяції.

> **Зауваження** :
> 
> В отличие от многих функций по работе с изображениями,**imagescale()** не змінює переданий параметр `image`; замість нього буде повернуто *нове*изображение.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`width`

Ширина масштабування.

`height`

Висота масштабування зображення. Якщо цей параметр опущений або негативний, співвідношення сторін буде збережено.

`mode`

Одна из констант\*\*`IMG_NEAREST_NEIGHBOUR`\*\* **`IMG_BILINEAR_FIXED`** **`IMG_BICUBIC`** **`IMG_BICUBIC_FIXED`** або ще щось (буде використано два проходи).

> **Зауваження** **`IMG_WEIGHTED4`** поки що не підтримується.

### Значення, що повертаються

Повертає об'єкт масштабованого зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Дивіться також

-   [imagecopyresized()](function.imagecopyresized.md) \- Копіювання та зміна розміру частини зображення
-   [imagecopyresampled()](function.imagecopyresampled.md) \- Копіювання та зміна розміру зображення з ресемплюванням
