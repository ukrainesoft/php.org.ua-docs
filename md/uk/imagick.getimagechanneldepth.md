---
navigation:
  - imagick.getimagebordercolor.md: '« Imagick::getImageBorderColor'
  - imagick.getimagechanneldistortion.md: 'Imagick::getImageChannelDistortion »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelDepth'
---
# Imagick::getImageChannelDepth

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelDepth — Повертає глибину для певного каналу зображення

### Опис

```methodsynopsis
public Imagick::getImageChannelDepth(int $channel): int
```

Повертає глибину для певного каналу зображення.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
