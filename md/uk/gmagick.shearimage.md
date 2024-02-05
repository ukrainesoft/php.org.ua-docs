---
navigation:
  - gmagick.setsize.md: '« Gmagick::setsize'
  - gmagick.solarizeimage.md: 'Gmagick::solarizeimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::shearimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::shearimage

(PECL gmagick >= Unknown)

Gmagick::shearimage — Створює паралелограм

### Опис

```methodsynopsis
public Gmagick::shearimage(mixed $color, float $xShear, float $yShear): Gmagick
```

Зсуває один край зображення по осі X або Y, утворюючи паралелограм. Зсув в напрямку X зсуває край осі X, а зсув в напрямку Y переміщує край осі Y. Величина зсуву контролюється кутом зсуву. Для зсуву в напрямку X xShear вимірюється щодо осі Y і аналогічним чином для зсуву в напрямку Y yShear вимірюється щодо осі X. Порожні трикутники, що залишилися від обрізки зображення, заповнюються кольором фону.

### Список параметрів

`color`

Піксельна паличка фону.

`xShear`

Число градусів для зсуву зображення на осі X.

`yShear`

Число градусів для зсуву зображення по осі Y.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
