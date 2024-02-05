---
navigation:
  - imagick.setpage.md: '« Imagick::setPage'
  - imagick.setprogressmonitor.md: 'Imagick::setProgressMonitor »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setPointSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setPointSize

(PECL imagick 2 >= 2.1.0, PECL imagick 3)

Imagick::setPointSize — Встановлює розмір точки

### Опис

```methodsynopsis
public Imagick::setPointSize(float $point_size): bool
```

Встановлює об'єкт властивість розміру точки. Метод можна використовувати, наприклад, для встановлення розміру шрифту для caption: формат псевдозображень. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.7 або старшим.

### Список параметрів

`point_size`

Розмір точки.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::setPointSize()\*\*\*\*

Приклад використання Imagick::setPointSize

```php
<?php
/* Создание нового объекта Imagick */
$im = new Imagick();

/* Установка шрифта для объекта */
$im->setFont("example.ttf");

/* Установка размера */
$im->setPointSize(12);

/* Создание заголовка */
$im->newPseudoImage(100, 100, "caption:Hello");

/* Работа с изображением */
?>
```

### Дивіться також

-   [Imagick::getPointSize()](imagick.getpointsize.md) \- Повертає розмір точки
