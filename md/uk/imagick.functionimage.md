---
navigation:
  - imagick.frameimage.md: '« Imagick::frameImage'
  - imagick.fximage.md: 'Imagick::fxImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::functionImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::functionImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::functionImage — Застосовує функцію зображення

### Опис

```methodsynopsis
public Imagick::functionImage(int $function, array $arguments, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує арифметичний, реляційний чи логічний вираз до псевдозображення.

Смотрите также[» ImageMagick v6 Examples - Image Transformations — Function, Multi-Argument Evaluate](http://www.imagemagick.org/Usage/transform/#function)

Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.9 або старшим.

### Список параметрів

`function`

Обратитесь к списку[констант FUNCTION](imagick.constants.md#imagick.constants.function)

`arguments`

Масив аргументів передачі у цю функцію.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Створення синусоїдального градієнта**

```php
<?php
$imagick = new Imagick();
$imagick->newPseudoImage(200, 200, 'gradient:black-white');
$arguments = array(3, -90);
$imagick->functionImage(Imagick::FUNCTION_SINUSOID, $arguments);

header("Content-Type: image/png");
$imagick->setImageFormat("png");
echo $imagick->getImageBlob();
?>
```

Висновок наведеного прикладу буде схожим на:

![Результат створення синусоїдального градієнта](images/c0d23d2d6769e53e24a1b3136c064577-functionImage_sinusoidal.png)

**Приклад #2 Створення поліномного градієнта (4x^2 - 4x + 1)**

```php
<?php
$imagick = new Imagick();
$imagick->newPseudoImage(200, 200, 'gradient:black-white');
$arguments = array(4, -4, 1);
$imagick->functionImage(Imagick::FUNCTION_POLYNOMIAL, $arguments);

header("Content-Type: image/png");
$imagick->setimageformat("png");
echo $imagick->getImageBlob();
?>
```

Висновок наведеного прикладу буде схожим на:

![Результат створення поліноміального градієнта](images/c0d23d2d6769e53e24a1b3136c064577-functionImage_polynomial.png)

**Приклад #3 Створення складного градієнта з полінома (4x^2 - 4x^2 + 1), модульованого синусоїдальним градієнтом**

```php
<?php
$imagick1 = new Imagick();
$imagick1->newPseudoImage(200, 200, 'gradient:black-white');
$arguments = array(9, -90);
$imagick1->functionImage(Imagick::FUNCTION_SINUSOID, $arguments);

$imagick2 = new Imagick();
$imagick2->newPseudoImage(200, 200, 'gradient:black-white');
$arguments = array(0.5, 0);
$imagick2->functionImage(Imagick::FUNCTION_SINUSOID, $arguments);
$imagick1->compositeimage($imagick2, Imagick::COMPOSITE_MULTIPLY, 0, 0);

header("Content-Type: image/png");
$imagick1->setImageFormat("png");
echo $imagick1->getImageBlob();
?>
```

Висновок наведеного прикладу буде схожим на:

![Результат створення складного градієнта](images/c0d23d2d6769e53e24a1b3136c064577-functionImage_multiplied.png)
