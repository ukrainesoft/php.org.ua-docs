---
navigation:
  - imagick.getimagechanneldistortion.md: '« Imagick::getImageChannelDistortion'
  - imagick.getimagechannelextrema.md: 'Imagick::getImageChannelExtrema »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageChannelDistortions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageChannelDistortions

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::getImageChannelDistortions — Повертає спотворення каналу

### Опис

```methodsynopsis
public Imagick::getImageChannelDistortions(Imagick $reference, int $metric, int $channel = Imagick::CHANNEL_DEFAULT): float
```

Порівнює один або кілька каналів зображення з відновленим зображенням та повертає зазначений показник спотворення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.4 або старшим.

### Список параметрів

`reference`

Об'єкт Imagick, що містить зображення, з яким проводиться порівняння.

`metric`

Зверніться до цього списку [констант типу METRIC](imagick.constants.md#imagick.constants.metric)

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно \*\*`Imagick::CHANNEL_DEFAULT`\*\*Обратитесь к списку[констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

Повертає число з плаваючою точкою (float), що описує спотворення каналу.

### Помилки

Викликає ImagickException у разі виникнення помилки.
