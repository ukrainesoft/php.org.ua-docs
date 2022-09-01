---
navigation:
  - gmagick.solarizeimage.md: '« Gmagick::solarizeimage'
  - gmagick.stripimage.md: 'Gmagick::stripimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::spreadimage'
---
# Gmagick::spreadimage

(PECL gmagick >= Unknown)

Gmagick::spreadimage — Випадково зміщує кожен піксель у блоці

### Опис

```methodsynopsis
public Gmagick::spreadimage(float $radius): Gmagick
```

Метод спеціальних ефектів, який випадково зміщує кожен піксель у блоці, заданому параметром radius.

### Список параметрів

`radius`

Виберіть випадковий піксель на околиці цього простору.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
