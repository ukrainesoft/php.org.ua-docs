---
navigation:
  - function.imagesetclip.md: « imagesetclip
  - function.imagesetpixel.md: imagesetpixel »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagesetinterpolation
---
# imagesetinterpolation

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imagesetinterpolation — Встановлює метод інтерполяції

### Опис

```methodsynopsis
imagesetinterpolation(GdImage $image, int $method = IMG_BILINEAR_FIXED): bool
```

Встановлює метод інтерполяції, встановлення методу інтерполяції впливає на відображення різних функцій GD, таких як функція [imagerotate()](function.imagerotate.md)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`method`

Метод інтерполяції, який може бути одним із наступних:

-   **`IMG_BELL`**: Фільтр Белла.
-   **`IMG_BESSEL`**: Фільтр Бесселя.
-   **`IMG_BICUBIC`**: Бікубічна інтерполяція
-   **`IMG_BICUBIC_FIXED`**: Фіксована точка реалізації бікубічної інтерполяції
-   **`IMG_BILINEAR_FIXED`**: Реалізація білінійної інтерполяції з фіксованою комою (`по умолчанию (также при создании изображения)`
-   **`IMG_BLACKMAN`**: Віконна функція Блекмана
-   **`IMG_BOX`**: Фільтр Коробка розмиття.
-   **`IMG_BSPLINE`**: Сплайн-інтерполяція.
-   **`IMG_CATMULLROM`**: Кубічна ермітова сплайн-інтерполяція
-   **`IMG_GAUSSIAN`**: Гаусова функція.
-   **`IMG_GENERALIZED_CUBIC`**: Узагальнена кубічна сплайн-фрактальна інтерполяція
-   **`IMG_HERMITE`**: Інтерполяція Ерміта
-   **`IMG_HAMMING`**: Фільтр Хеммінга.
-   **`IMG_HANNING`**: Фільтр Хеннінга.
-   **`IMG_MITCHELL`**: Фільтр Мітчелла.
-   **`IMG_POWER`**: Ступінна інтерполяція.
-   **`IMG_QUADRATIC`**: Зворотня квадратична інтерполяція
-   **`IMG_SINC`**: Синк функція.
-   **`IMG_NEAREST_NEIGHBOUR`**: Інтерполяція найближчого сусіда
-   **`IMG_WEIGHTED4`**: Ваговий фільтр.
-   **`IMG_TRIANGLE`**: Трикутна інтерполяція

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesetinterpolation()****

```php
<?php
// Загрузка изображения
$im = imagecreate(500, 500);

// По умолчанию интерполяция IMG_BILINEAR_FIXED, переключитесь
// на использование фильтра 'Митчелла':
imagesetinterpolation($im, IMG_MITCHELL);

// Continue to work with $im ...
?>
```

### Примітки

Зміна методу інтерполяції впливає на такі функції при відображенні:

-   [imageaffine()](function.imageaffine.md)
-   [imagerotate()](function.imagerotate.md)

### Дивіться також

-   [imagegetinterpolation()](function.imagegetinterpolation.md) - Отримує метод інтерполяції
