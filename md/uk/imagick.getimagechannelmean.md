---
navigation:
  - imagick.getimagechannelkurtosis.md: '« Imagick::getImageChannelKurtosis'
  - imagick.getimagechannelrange.md: 'Imagick::getImageChannelRange »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelMean'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

Повертає масив із елементами `"mean"`и`"standardDeviation"`

### Помилки

Викликає ImagickException у разі виникнення помилки.
