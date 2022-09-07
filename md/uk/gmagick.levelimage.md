---
navigation:
  - gmagick.labelimage.md: '« Gmagick::labelimage'
  - gmagick.magnifyimage.md: 'Gmagick::magnifyimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::levelimage'
---
# Gmagick::levelimage

(PECL gmagick >= Unknown)

Gmagick::levelimage — Регулює рівні зображення

### Опис

```methodsynopsis
public Gmagick::levelimage(    float $blackPoint,    float $gamma,    float $whitePoint,    int $channel = Gmagick::CHANNEL_DEFAULT): mixed
```

Регулює рівні зображення, масштабуючи кольори, що потрапляють між зазначеними білими та чорними точками, до доступного квантового діапазону. Надані параметри є чорними, середніми і білими точками. Чорна точка вказує на темний колір зображення. Кольори темніші за крапку чорного встановлюються на нуль. Середня точка визначає гамма-корекцію, що застосовується до зображення. Біла точка визначає найсвітліший колір зображення. Кольори яскравіші за крапку білого встановлюються на максимальне квантове значення.

### Список параметрів

`blackPoint`

Чорна точка зображення.

`gamma`

Значення гами.

`whitePoint`

Білий точки зображення.

`channel`

Вкажіть будь-яку константу каналу, яка є дійсною для вашого режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до списку [констант канала](gmagick.constants.md#gmagick.constants.channel)

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) із вирівняним зображенням.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
