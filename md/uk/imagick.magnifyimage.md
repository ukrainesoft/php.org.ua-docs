---
navigation:
  - imagick.listregistry.md: '« Imagick::listRegistry'
  - imagick.mapimage.md: 'Imagick::mapImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::magnifyImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::magnifyImage

(PECL imagick 2, PECL imagick 3)

Imagick::magnifyImage — Пропорційно масштабує зображення вдвічі

### Опис

```methodsynopsis
public Imagick::magnifyImage(): bool
```

Масштабує зображення вдвічі пропорційно оригінальному розміру.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::magnifyImage()\*\*\*\*

```php
<?php
function magnifyImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->magnifyImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
