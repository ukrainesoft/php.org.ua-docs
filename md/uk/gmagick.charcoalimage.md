---
navigation:
  - gmagick.borderimage.md: '« Gmagick::borderimage'
  - gmagick.chopimage.md: 'Gmagick::chopimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::charcoalimage'
---
# Gmagick::charcoalimage

(PECL gmagick >= Unknown)

Gmagick::charcoalimage — Імітація малювання вугіллям

### Опис

```methodsynopsis
public Gmagick::charcoalimage(float $radius, float $sigma): Gmagick
```

Імітація малювання вугіллям.

### Список параметрів

`radius`

Радіус гауссіани в пікселях, крім центрального пікселя.

`sigma`

Стандартне відхилення гауссіани у пікселях.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) з доданим ефектом малювання вугіллям.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
