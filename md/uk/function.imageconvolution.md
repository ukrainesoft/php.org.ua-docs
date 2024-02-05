---
navigation:
  - function.imagecolortransparent.md: « imagecolortransparent
  - function.imagecopy.md: imagecopy »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageconvolution
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imageconvolution

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

imageconvolution — Накладення матриці 3х3, що викривляє, використовуючи коефіцієнт і зсув

### Опис

```methodsynopsis
imageconvolution(    GdImage $image,    array $matrix,    float $divisor,    float $offset): bool
```

Накладає матрицю, що викривляє, на зображення, використовуючи заданий коефіцієнт і зсув.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`matrix`

Матриця 3x3: масив із трьох масивів по 3 значення з плаваючою точкою в кожному.

`divisor`

Дільник результату викривлення, що використовується для нормалізації.

`offset`

Зміщення кольорів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Створення рельєфу на логотипі PHP.net**

```php
<?php
$image = imagecreatefromgif('http://www.php.net/images/php.gif');

$emboss = array(array(2, 0, 0), array(0, -1, 0), array(0, 0, -1));
imageconvolution($image, $emboss, 1, 127);

header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

Результат виконання наведеного прикладу:

![Висновок прикладу: Створення рельєфу на логотипі PHP.net](images/21009b70229598c6a80eef8b45bf282b-imageconvolution_emboss.png)

**Приклад #2 Розмиття по Гаусу**

```php
<?php
$image = imagecreatetruecolor(180,40);

// Пишет текст и применяет размытие к изображению
imagestring($image, 5, 10, 8, 'Gaussian Blur Text', 0x00ff00);
$gaussian = array(array(1.0, 2.0, 1.0), array(2.0, 4.0, 2.0), array(1.0, 2.0, 1.0));
imageconvolution($image, $gaussian, 16, 0);

// Переписывает текст для сравнения
imagestring($image, 5, 10, 18, 'Gaussian Blur Text', 0x00ff00);

header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

Результат виконання наведеного прикладу:

![Висновок прикладу: Розмиття за Гаусом](images/21009b70229598c6a80eef8b45bf282b-imageconvolution_gaussian.png)

### Дивіться також

-   [imagefilter()](function.imagefilter.md) \- Застосовує фільтр до зображення
