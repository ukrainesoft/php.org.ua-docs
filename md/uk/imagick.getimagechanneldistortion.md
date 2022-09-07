---
navigation:
  - imagick.getimagechanneldepth.md: '« Imagick::getImageChannelDepth'
  - imagick.getimagechanneldistortions.md: 'Imagick::getImageChannelDistortions »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelDistortion'
---
# Imagick::getImageChannelDistortion

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelDistortion — Порівнює канали зображення з відновленим зображенням

### Опис

```methodsynopsis
public Imagick::getImageChannelDistortion(Imagick $reference, int $channel, int $metric): float
```

Порівнює один або кілька каналів зображення з відновленим зображенням та повертає зазначений показник спотворення.

### Список параметрів

`reference`

Об'єкт Imagick для порівняння.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

`metric`

Одна з [констант типа METRIC](imagick.constants.md#imagick.constants.metric)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
