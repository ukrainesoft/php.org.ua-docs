---
navigation:
  - imagick.commentimage.md: '« Imagick::commentImage'
  - imagick.compareimagelayers.md: 'Imagick::compareImageLayers »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::compareImageChannels'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::compareImageChannels

(PECL imagick 2, PECL imagick 3)

Imagick::compareImageChannels — Повертає різницю в одному або кількох зображеннях

### Опис

```methodsynopsis
public Imagick::compareImageChannels(Imagick $image, int $channelType, int $metricType): array
```

Порівнює одне або кілька зображень та повертає різницеве ​​зображення.

### Список параметрів

`image`

Об'єкт Imagick, що містить зображення для порівняння.

`channelType`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.md#imagick.constants.channel)

`metricType`

Одна из[констант типу METRIC](imagick.constants.md#imagick.constants.metric)

### Значення, що повертаються

Масив, що складається з `new_wand`и`distortion`

### Помилки

Викликає ImagickException у разі виникнення помилки.
