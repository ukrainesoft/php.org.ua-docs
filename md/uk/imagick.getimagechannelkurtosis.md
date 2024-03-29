---
navigation:
  - imagick.getimagechannelextrema.md: '« Imagick::getImageChannelExtrema'
  - imagick.getimagechannelmean.md: 'Imagick::getImageChannelMean »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelKurtosis'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageChannelKurtosis

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::getImageChannelKurtosis — Повертає ексцес та асиметрію певного каналу

### Опис

```methodsynopsis
public Imagick::getImageChannelKurtosis(int $channel = Imagick::CHANNEL_DEFAULT): array
```

Повертає ексцес та асиметрію певного каналу. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.9 або старшим.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно \*\*`Imagick::CHANNEL_DEFAULT`\*\*Обратитесь к списку[констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

Повертає масив із елементами `kurtosis`и`skewness`

### Помилки

Викликає ImagickException у разі виникнення помилки.
