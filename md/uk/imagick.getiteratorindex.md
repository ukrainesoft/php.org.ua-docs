---
navigation:
  - imagick.getinterlacescheme.md: '« Imagick::getInterlaceScheme'
  - imagick.getnumberimages.md: 'Imagick::getNumberImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getIteratorIndex'
---
# Imagick::getIteratorIndex

(PECL imagick 2, PECL imagick 3)

Imagick::getIteratorIndex — Повертає індекс активного поточного зображення.

### Опис

```methodsynopsis
public Imagick::getIteratorIndex(): int
```

Повертає індекс активного поточного зображення в об'єкті Imagick. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що містить індекс зображення у стеку.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::getIteratorIndex()****

Створення зображення, встановлення та отримання індексу ітератора

```php
<?php
$im = new Imagick();
$im->newImage(100, 100, new ImagickPixel("red"));
$im->newImage(100, 100, new ImagickPixel("green"));
$im->newImage(100, 100, new ImagickPixel("blue"));

$im->setIteratorIndex(1);
echo $im->getIteratorIndex();
?>
```

### Дивіться також

-   [Imagick::setIteratorIndex()](imagick.setiteratorindex.md) - встановлює позицію ітератора
-   [Imagick::getImageIndex()](imagick.getimageindex.md) - Повертає індекс поточного активного зображення
-   [Imagick::setImageIndex()](imagick.setimageindex.md) - встановлює позицію ітератора
