---
navigation:
  - imagick.extentimage.md: '« Imagick::extentImage'
  - imagick.flattenimages.md: 'Imagick::flattenImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::filter'
---
# Imagick::filter

(PECL imagick 3> = 3.3.0)

Imagick::filter — Опис

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::filter(ImagickKernel $ImagickKernel, int $channel = Imagick::CHANNEL_UNDEFINED): bool
```

Застосовує ядро ​​користувача згортки до зображення.

### Список параметрів

`ImagickKernel`

Примірник ImagickKernel, який представляє або одне ядро, або пов'язану серію ядер.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::filter()****

```php
<?php
function filter($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $matrix = [
        [-1, 0, -1],
        [0,  5,  0],
        [-1, 0, -1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);
    $strength = 0.5;
    $kernel->scale($strength, \Imagick::NORMALIZE_KERNEL_VALUE);
    $kernel->addUnityKernel(1 - $strength);

    $imagick->filter($kernel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
