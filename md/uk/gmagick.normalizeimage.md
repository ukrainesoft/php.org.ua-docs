---
navigation:
  - gmagick.nextimage.md: '« Gmagick::nextimage'
  - gmagick.oilpaintimage.md: 'Gmagick::oilpaintimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::normalizeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
