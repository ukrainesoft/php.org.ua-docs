---
navigation:
  - imagick.getimagechannelmean.md: '« Imagick::getImageChannelMean'
  - imagick.getimagechannelstatistics.md: 'Imagick::getImageChannelStatistics »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelRange'
---
# Imagick::getImageChannelRange

(PECL imagick 2> = 2.2.1, PECL imagick 3)

Imagick::getImageChannelRange — Повертає діапазон каналів

### Опис

```methodsynopsis
public Imagick::getImageChannelRange(int $channel): array
```

Повертає діапазон для одного або кількох каналів зображення. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.4.0 або старшим.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

Повертає масив, що містить мінімальні та максимальні значення каналу(ів).

### Помилки

Викликає ImagickException у разі виникнення помилки.
