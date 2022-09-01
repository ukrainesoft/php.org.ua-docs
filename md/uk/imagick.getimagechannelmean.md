---
navigation:
  - imagick.getimagechannelkurtosis.html: '« Imagick::getImageChannelKurtosis'
  - imagick.getimagechannelrange.html: 'Imagick::getImageChannelRange »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::getImageChannelMean'
---
# Imagick::getImageChannelMean

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelMean — Повертає середнє та стандартне відхилення

### Опис

```methodsynopsis
public Imagick::getImageChannelMean(int $channel): array
```

Повертає середнє та стандартне відхилення одного або кількох каналів зображення.

### Список параметрів

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

Повертає масив із елементами `"mean"` і `"standardDeviation"`

### Помилки

Викликає ImagickException у разі виникнення помилки.
