---
navigation:
  - imagick.settype.md: '« Imagick::setType'
  - imagick.shadowimage.md: 'Imagick::shadowImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::shadeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::shadeImage

(PECL imagick 2, PECL imagick 3)

Imagick::shadeImage — Створює 3D-ефект

### Опис

```methodsynopsis
public Imagick::shadeImage(bool $gray, float $azimuth, float $elevation): bool
```

Світить дальнє світло на зображення для створення тривимірного ефекту. Ви керуєте розташуванням джерела світла за допомогою азимуту та піднесення; азимут вимірюється в градусах від осі X, а висота вимірюється в пікселях над віссю Z. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`gray`

Значення, відмінне від нуля, відтінює інтенсивність кожного пікселя.

`azimuth`

Визначає напрямок джерела світла.

`elevation`

Визначає напрямок джерела світла.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викидає виняток ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::shadeImage()\*\*\*\*

```php
<?php
function shadeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->shadeImage(true, 45, 20);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
