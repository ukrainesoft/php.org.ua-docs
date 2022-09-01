---
navigation:
  - imagick.smushimages.md: '« Imagick::smushImages'
  - imagick.sparsecolorimage.md: 'Imagick::sparseColorImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::solarizeImage'
---
# Imagick::solarizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::solarizeImage — Застосовує до зображення ефект соляризації

### Опис

```methodsynopsis
public Imagick::solarizeImage(int $threshold): bool
```

Застосовує до зображення спеціальний ефект, аналогічний ефекту, що досягається у фотолабораторії шляхом вибіркового впливу світла на ділянки фоточутливого паперу. Поріг варіюється від 0 до QuantumRange і є мірою соляризації.

### Список параметрів

`threshold`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::solarizeImage()****

```php
<?php
function solarizeImage($imagePath, $solarizeThreshold) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->solarizeImage($solarizeThreshold * \Imagick::getQuantum());
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
