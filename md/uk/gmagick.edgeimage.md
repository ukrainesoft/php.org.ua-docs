---
navigation:
  - gmagick.drawimage.html: '« Gmagick::drawimage'
  - gmagick.embossimage.html: 'Gmagick::embossimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::edgeimage'
---
# Gmagick::edgeimage

(PECL gmagick >= Unknown)

Gmagick::edgeimage — Збільшує краї зображення.

### Опис

```methodsynopsis
public Gmagick::edgeimage(float $radius): Gmagick
```

Збільшує краї зображення за допомогою фільтра згортки даного радіуса. Використовуйте радіус 0, і його буде обрано автоматично.

### Список параметрів

`radius`

Радіус операції.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) із збільшеними краями.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
