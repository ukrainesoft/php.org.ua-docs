---
navigation:
  - gmagick.nextimage.md: '« Gmagick::nextimage'
  - gmagick.oilpaintimage.md: 'Gmagick::oilpaintimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::normalizeimage'
---
# Gmagick::normalizeimage

(PECL gmagick >= Unknown)

Gmagick::normalizeimage — Підвищує контрастність кольорового зображення

### Опис

```methodsynopsis
public Gmagick::normalizeimage(int $channel = ?): Gmagick
```

Підвищує контраст кольорового зображення, регулюючи колір пікселів для охоплення всього діапазону доступних кольорів.

### Список параметрів

`channel`

Визначає який канал нормалізувати.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
