---
navigation:
  - imagick.newimage.md: '« Imagick::newImage'
  - imagick.nextimage.md: 'Imagick::nextImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::newPseudoImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::newPseudoImage

(PECL imagick 2, PECL imagick 3)

Imagick::newPseudoImage — Створює нове зображення

### Опис

```methodsynopsis
public Imagick::newPseudoImage(int $columns, int $rows, string $pseudoString): bool
```

Створює нове зображення за допомогою псевдоформатів ImageMagick.

### Список параметрів

`columns`

Стовпці у новому зображенні.

`rows`

Рядки у новому зображенні.

`pseudoString`

Рядок, що містить визначення псевдозображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::newPseudoImage()\*\*\*\*

```php
<?php
function newPseudoImage($canvasType) {
    $imagick = new \Imagick();
    $imagick->newPseudoImage(300, 300, $canvasType);
    $imagick->setImageFormat("png");
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

//newPseudoImage('gradient:red-rgba(64, 255, 255, 0.5)');
//newPseudoImage("radial-gradient:red-blue");
newPseudoImage("plasma:fractal");

?>
```
