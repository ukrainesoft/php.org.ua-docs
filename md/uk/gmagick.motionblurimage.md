---
navigation:
  - gmagick.modulateimage.md: '« Gmagick::modulateimage'
  - gmagick.newimage.md: 'Gmagick::newimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::motionblurimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::motionblurimage

(PECL gmagick >= Unknown)

Gmagick::motionblurimage — Імітує розмиття під час руху

### Опис

```methodsynopsis
public Gmagick::motionblurimage(float $radius, float $sigma, float $angle): Gmagick
```

Імітує розмиття під час руху. Згортає зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (sigma). Для отримання прийнятних результатів radius повинен бути більшим за sigma. При використанні значення radius, що дорівнює 0, **Gmagick::motionblurimage()** вибере вам відповідний радіус. Параметр angle задає кут розмиття руху.

### Список параметрів

`radius`

Радіус у пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення у пікселях.

`angle`

Кут, під яким застосовується ефект.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
