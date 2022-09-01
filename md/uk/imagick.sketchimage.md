---
navigation:
  - imagick.sigmoidalcontrastimage.md: '« Imagick::sigmoidalContrastImage'
  - imagick.smushimages.md: 'Imagick::smushImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::sketchImage'
---
# Imagick::sketchImage

(PECL imagick 2, PECL imagick 3)

Imagick::sketchImage — Імітує малюнок олівцем

### Опис

```methodsynopsis
public Imagick::sketchImage(float $radius, float $sigma, float $angle): bool
```

Імітує малюнок олівцем. Зображення згортається за допомогою гаусівського оператора, заданого радіусу та стандартного відхилення (сигма). Для розумних результатів радіус має бути більшим за сигму. Використовуйте радіус 0, щоб Imagick::sketchImage() використовувала відповідний радіус самостійно. Кут задає кут розмиття руху. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`radius`

Радіус гауссіани в пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення гауссіани у пікселях.

`angle`

Застосовується ефект під вказаним кутом.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::sketchImage()****

```php
<?php
function sketchImage($imagePath, $radius, $sigma, $angle) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->sketchimage($radius, $sigma, $angle);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
