---
navigation:
  - imagick.motionblurimage.md: '« Imagick::motionBlurImage'
  - imagick.newimage.md: 'Imagick::newImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::negateImage'
---
# Imagick::negateImage

(PECL imagick 2, PECL imagick 3)

Imagick::negateImage — Інвертує кольори в еталонному зображенні

### Опис

```methodsynopsis
public Imagick::negateImage(bool $gray, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Інвертує кольори у еталонному зображенні. Параметр Grayscale означає, що зображення інвертуються лише значення відтінків сірого.

### Список параметрів

`gray`

Визначає, чи потрібно інвертувати лише пікселі у відтінках сірого зображення.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для заданого режиму каналу. Для застосування більш ніж одного каналу необхідно об'єднати константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::negateImage()****

```php
<?php
function negateImage($imagePath, $grayOnly, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->negateImage($grayOnly, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
