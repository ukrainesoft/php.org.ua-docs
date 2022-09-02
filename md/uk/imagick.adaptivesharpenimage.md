---
navigation:
  - imagick.adaptiveresizeimage.md: '« Imagick::adaptiveResizeImage'
  - imagick.adaptivethresholdimage.md: 'Imagick::adaptiveThresholdImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::adaptiveSharpenImage'
---
# Imagick::adaptiveSharpenImage

(PECL imagick 2, PECL imagick 3)

Imagick::adaptiveSharpenImage — Адаптивна зміна різкості зображення

### Опис

```methodsynopsis
public Imagick::adaptiveSharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Адаптивна зміна різкості зображення з більшою інтенсивністю на краях зображення та з меншою ближче до середини. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`radius`

Радіус Гауса, у пікселях, крім центрального пікселя. Використовуйте 0 для автовибору.

`sigma`

Стандартне відхилення Гауса, у пікселях.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::adaptiveSharpenImage()****

Адаптивна зміна різкості зображення з радіусом 2 та сигмою 1.

```php
<?php
try {
    $image = new Imagick('image.png');
    $image->adaptiveSharpenImage(2,1);
} catch(ImagickException $e) {
    echo 'Ошибка: ' , $e->getMessage();
    die();
}
header('Content-type: image/png');
echo $image;
?>
```

### Дивіться також

-   [Imagick::sharpenImage()](imagick.sharpenimage.md) - Підвищує різкість зображення
