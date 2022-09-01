---
navigation:
  - imagick.optimizeimagelayers.md: '« Imagick::optimizeImageLayers'
  - imagick.paintfloodfillimage.md: 'Imagick::paintFloodfillImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::orderedPosterizeImage'
---
# Imagick::orderedPosterizeImage

(PECL imagick 2> = 2.2.2, PECL imagick 3)

Imagick::orderedPosterizeImage — Виконує впорядкований дизеринг

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::orderedPosterizeImage(string $threshold_map, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Виконує впорядкований дизеринг на основі ряду визначених карток порогових значень дизерингу, але з кількома рівнями інтенсивності, які можуть бути різними для різних каналів відповідно до вхідних аргументів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.1 або старшим.

### Список параметрів

`threshold_map`

Рядок, що містить ім'я порогового дизерингу, що використовується.

`channel`

Вкажіть будь-яку константу каналу, яка є дійсною для вашого режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до списку [констант канала](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::orderedPosterizeImage()****

```php
<?php
function orderedPosterizeImage($imagePath, $orderedPosterizeType) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->orderedPosterizeImage($orderedPosterizeType);
    $imagick->setImageFormat('png');

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

//orderedPosterizeImage($imagePath, 'o4x4,3,3');
//orderedPosterizeImage($imagePath, 'o8x8,6,6');
orderedPosterizeImage($imagePath, 'h8x8a');
?>
```
