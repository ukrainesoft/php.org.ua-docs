---
navigation:
  - imagick.getimageiterations.md: '« Imagick::getImageIterations'
  - imagick.getimagematte.md: 'Imagick::getImageMatte »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageLength'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageLength

(PECL imagick 2, PECL imagick 3)

Imagick::getImageLength — Повертає довжину зображення в байтах

### Опис

```methodsynopsis
public Imagick::getImageLength(): int
```

Повертає довжину зображення у байтах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що містить поточний розмір зображення.

### Приклади

**Пример #1 Пример использования**Imagick::getImageLength()\*\* :\*\*

Отримання довжини зображення в байтах

```php
<?php
$image = new Imagick('test.jpg');
echo $image->getImageLength() . ' байт';
?>
```
