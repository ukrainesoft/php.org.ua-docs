---
navigation:
  - imagick.construct.md: '« Imagick::\_\_construct'
  - imagick.contraststretchimage.md: 'Imagick::contrastStretchImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::contrastImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::contrastImage

(PECL imagick 2, PECL imagick 3)

Imagick::contrastImage — Змінює контраст зображення

### Опис

```methodsynopsis
public Imagick::contrastImage(bool $sharpen): bool
```

Збільшує різницю в інтенсивності між світлими та темними елементами зображення. Встановіть збільшення різкості на значення, відмінне від 0, щоб збільшити контраст зображення, інакше контраст зменшується.

### Список параметрів

`sharpen`

Значення різкості

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::contrastImage()\*\*\*\*

```php
<?php
function contrastImage($imagePath, $contrastType) {
    $imagick = new \Imagick(realpath($imagePath));
    if ($contrastType != 2) {
        $imagick->contrastImage($contrastType);
    }

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
