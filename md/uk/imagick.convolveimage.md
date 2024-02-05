---
navigation:
  - imagick.contraststretchimage.md: '« Imagick::contrastStretchImage'
  - imagick.count.md: 'Imagick::count »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::convolveImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::convolveImage

(PECL imagick 2, PECL imagick 3)

Imagick::convolveImage — Застосовує ядро ​​згортки для користувача.

### Опис

```methodsynopsis
public Imagick::convolveImage(array $kernel, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовується ядро ​​згортки до зображення.

### Список параметрів

`kernel`

Ядро згортки.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів.Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::convolveImage()\*\*\*\*

```php
<?php
function convolveImage($imagePath, $bias, $kernelMatrix) {
    $imagick = new \Imagick(realpath($imagePath));
    //$edgeFindingKernel = [-1, -1, -1, -1, 8, -1, -1, -1, -1,];
    $imagick->setImageBias($bias * \Imagick::getQuantum());
    $imagick->convolveImage($kernelMatrix);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
