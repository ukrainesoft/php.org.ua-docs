---
navigation:
  - imagick.recolorimage.md: '« Imagick::recolorImage'
  - imagick.remapimage.md: 'Imagick::remapImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::reduceNoiseImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::reduceNoiseImage

(PECL imagick 2, PECL imagick 3)

Imagick::reduceNoiseImage — Згладжує контури зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::reduceNoiseImage(float $radius): bool
```

Згладжує контури зображення, зберігаючи при цьому інформацію про краї. Алгоритм працює, замінюючи кожен піксель найближчим за значенням сусідом. Сусід визначається радіусом. При використанні радіуса 0, Imagick::reduceNoiseImage() вибере відповідний радіус автоматично.

### Список параметрів

`radius`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::reduceNoiseImage()\*\*\*\*

```php
<?php
function reduceNoiseImage($imagePath, $reduceNoise) {
    $imagick = new \Imagick(realpath($imagePath));
    @$imagick->reduceNoiseImage($reduceNoise);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
