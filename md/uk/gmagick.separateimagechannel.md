---
navigation:
  - gmagick.scaleimage.md: '« Gmagick::scaleimage'
  - gmagick.setcompressionquality.md: 'Gmagick::setCompressionQuality »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::separateimagechannel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::separateimagechannel

(PECL gmagick >= Unknown)

Gmagick::separateimagechannel — Відокремлює канал від зображення.

### Опис

```methodsynopsis
public Gmagick::separateimagechannel(int $channel): Gmagick
```

Відокремлює канал від зображення та повертає зображення у відтінках сірого. Канал – це певний колірний компонент кожного пікселя зображення.

### Список параметрів

`channel`

Одна из констант[каналу](gmagick.constants.md#gmagick.constants.channel) `Gmagick::CHANNEL_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
