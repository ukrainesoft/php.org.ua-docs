---
navigation:
  - imagick.setinterlacescheme.md: '« Imagick::setInterlaceScheme'
  - imagick.setlastiterator.md: 'Imagick::setLastIterator »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setIteratorIndex'
---
# Imagick::setIteratorIndex

(PECL imagick 2, PECL imagick 3)

Imagick::setIteratorIndex — Встановлює позицію ітератора

### Опис

```methodsynopsis
public Imagick::setIteratorIndex(int $index): bool
```

Встановлює ітератор у позицію списку зображень, вказану за допомогою параметра index. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`index`

Позиція встановлення ітератора.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setIteratorIndex()****

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

-   [Imagick::getIteratorIndex()](imagick.getiteratorindex.md) - Повертає індекс поточного активного зображення
-   [Imagick::getImageIndex()](imagick.getimageindex.md) - Повертає індекс поточного активного зображення
-   [Imagick::setImageIndex()](imagick.setimageindex.md) - встановлює позицію ітератора
