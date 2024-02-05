---
navigation:
  - gmagick.drawimage.md: '« Gmagick::drawimage'
  - gmagick.embossimage.md: 'Gmagick::embossimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::edgeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Об'єкт [Gmagick](class.gmagick.md) із збільшеними краями.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
