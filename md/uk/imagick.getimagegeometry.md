---
navigation:
  - imagick.getimagegamma.md: '« Imagick::getImageGamma'
  - imagick.getimagegravity.md: 'Imagick::getImageGravity »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageGeometry'
---
# Imagick::getImageGeometry

(PECL imagick 2, PECL imagick 3)

Imagick::getImageGeometry — Повертає ширину та висоту у вигляді асоціативного масиву

### Опис

```methodsynopsis
public Imagick::getImageGeometry(): array
```

Повертає ширину та висоту у вигляді асоціативного масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із шириною та висотою зображення.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::getImageGeometry()****

```php
<?php
$imagick = new Imagick();
$imagick->newImage(100, 200, "black");
print_r($imagick->getImageGeometry());
?>
```

Результат виконання цього прикладу:

```
Array
(
    [width] => 100
    [height] => 200
)
```
