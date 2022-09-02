---
navigation:
  - gmagick.stripimage.md: '« Gmagick::stripimage'
  - gmagick.thumbnailimage.md: 'Gmagick::thumbnailimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::swirlimage'
---
# Gmagick::swirlimage

(PECL gmagick >= Unknown)

Gmagick::swirlimage — Закручує пікселі навколо центру зображення

### Опис

```methodsynopsis
public Gmagick::swirlimage(float $degrees): Gmagick
```

Закручує пікселі навколо центру зображення, де градуси вказують розмах дуги, якою переміщається кожен піксель. Ви отримуєте драматичніший ефект, коли градуси переміщуються від 1 до 360.

### Список параметрів

`degrees`

Визначає герметичність закрученого ефекту.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
