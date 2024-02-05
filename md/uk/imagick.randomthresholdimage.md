---
navigation:
  - imagick.raiseimage.md: '« Imagick::raiseImage'
  - imagick.readimage.md: 'Imagick::readImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::randomThresholdImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::randomThresholdImage

(PECL imagick 2, PECL imagick 3)

Imagick::randomThresholdImage — Створює висококонтрастне двокольорове зображення

### Опис

```methodsynopsis
public Imagick::randomThresholdImage(float $low, float $high, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює значення окремих пікселів залежно від інтенсивності кожного пікселя проти пороговим значенням. В результаті виходить висококонтрастне двоколірне зображення. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`low`

Нижня точка.

`high`

Верхня точка.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для заданого режиму каналу. Для застосування більш ніж одного каналу необхідно об'єднати константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::randomThresholdImage()\*\*\*\*

```php
<?php
function randomThresholdimage($imagePath, $lowThreshold, $highThreshold, $channel) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->randomThresholdimage(
        $lowThreshold * \Imagick::getQuantum(),
        $highThreshold * \Imagick::getQuantum(),
        $channel
    );
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
