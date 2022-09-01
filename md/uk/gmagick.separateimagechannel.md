---
navigation:
  - gmagick.scaleimage.html: '« Gmagick::scaleimage'
  - gmagick.setcompressionquality.html: 'Gmagick::setCompressionQuality »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::separateimagechannel'
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

Одна з констант [канала](gmagick.constants.html#gmagick.constants.channel) `Gmagick::CHANNEL_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
