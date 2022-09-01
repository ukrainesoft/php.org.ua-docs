---
navigation:
  - imagick.contraststretchimage.html: '« Imagick::contrastStretchImage'
  - imagick.count.html: 'Imagick::count »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::convolveImage'
---
# Imagick::convolveImage

(PECL imagick 2, PECL imagick 3)

Imagick::convolveImage — Застосовує ядро ​​згортки для користувача.

### Опис

```methodsynopsis
public Imagick::convolveImage(array $kernel, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує ядро ​​користувача згортки до зображення.

### Список параметрів

`kernel`

Ядро згортки.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів.Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::convolveImage()****

```php
<?php
function convolveImage($imagePath, $bias, $kernelMatrix) {
    $imagick = new \Imagick(realpath($imagePath));
    //$edgeFindingKernel = [-1, -1, -1, -1, 8, -1, -1, -1, -1,];
    $imagick->setImageBias($bias * \Imagick::getQuantum());
    $imagick->convolveImage($kernelMatrix);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
