---
navigation:
  - gmagick.readimagefile.md: '« Gmagick::readimagefile'
  - gmagick.removeimage.md: 'Gmagick::removeimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::reducenoiseimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::reducenoiseimage

(PECL gmagick >= Unknown)

Gmagick::reducenoiseimage — Згладжує контури зображення

### Опис

```methodsynopsis
public Gmagick::reducenoiseimage(float $radius): Gmagick
```

Згладжує контури зображення, зберігаючи при цьому інформацію про краї. Алгоритм працює, замінюючи кожен піксель найближчим за значенням сусідом. Сусід визначається значенням radius. Використовуйте значення radius, що дорівнює 0, і **Gmagick::reducenoiseimage()** вибере вам відповідний радіус.

### Список параметрів

`radius`

Радіус околиці пікселів.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
