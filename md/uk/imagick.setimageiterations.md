---
navigation:
  - imagick.setimageinterpolatemethod.md: '« Imagick::setImageInterpolateMethod'
  - imagick.setimagematte.md: 'Imagick::setImageMatte »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageIterations'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageIterations

(PECL imagick 2, PECL imagick 3)

Imagick::setImageIterations — Встановлює ітерацію зображення

### Опис

```methodsynopsis
public Imagick::setImageIterations(int $iterations): bool
```

Встановлює кількість ітерацій, коли анімоване зображення повторюється.

### Список параметрів

`iterations`

Число ітерацій, які зображення має повторити. Використовуйте '0' для безперервного повторення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::setImageIterations()\*\*\*\*

```php
<?php

$imagick = new Imagick(realpath("Test.gif"));

$imagick = $imagick->coalesceImages();
$imagick->setImageIterations(1);
$imagick = $imagick->deconstructImages();

$imagick->writeImages('/path/to/save/OnceOnly.gif', true);

?>
```
