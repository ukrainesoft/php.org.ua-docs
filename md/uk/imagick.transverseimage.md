---
navigation:
  - imagick.transposeimage.md: '« Imagick::transposeImage'
  - imagick.trimimage.md: 'Imagick::trimImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::transverseImage'
---
# Imagick::transverseImage

(PECL imagick 2, PECL imagick 3)

Imagick::transverseImage — Створює горизонтальне дзеркальне відображення

### Опис

```methodsynopsis
public Imagick::transverseImage(): bool
```

Створює горизонтальне дзеркальне зображення, відбиваючи пікселі навколо центральної осі Y, повертаючи їх у 270 градусів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::transverseImage()****

```php
<?php
function transverseImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->transverseImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::transposeImage()](imagick.transposeimage.md) - Створює вертикальне дзеркальне відображення
