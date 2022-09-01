---
navigation:
  - gmagick.nextimage.html: '« Gmagick::nextimage'
  - gmagick.oilpaintimage.html: 'Gmagick::oilpaintimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
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

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
