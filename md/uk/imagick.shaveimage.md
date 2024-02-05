---
navigation:
  - imagick.sharpenimage.md: '« Imagick::sharpenImage'
  - imagick.shearimage.md: 'Imagick::shearImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::shaveImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::shaveImage

(PECL imagick 2, PECL imagick 3)

Imagick::shaveImage — Видалення пікселів по краях зображення

### Опис

```methodsynopsis
public Imagick::shaveImage(int $columns, int $rows): bool
```

Видаляє пікселі на краях зображення. Метод виділяє пам'ять, необхідну нової структури зображення, і повертає покажчик на нове зображення.

### Список параметрів

`columns`

`rows`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::shaveImage()\*\*\*\*

```php
<?php
function shaveImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->shaveImage(100, 50);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
