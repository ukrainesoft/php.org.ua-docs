---
navigation:
  - gmagick.shearimage.md: '« Gmagick::shearimage'
  - gmagick.spreadimage.md: 'Gmagick::spreadimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::solarizeimage'
---
# Gmagick::solarizeimage

(PECL gmagick >= Unknown)

Gmagick::solarizeimage — Застосовує ефект соляризації до зображення.

### Опис

```methodsynopsis
public Gmagick::solarizeimage(int $threshold): Gmagick
```

Застосовує особливий ефект до зображення, подібний до ефекту, що досягається у фотолабораторії за допомогою вибіркового експонування областей світлочутливого паперу на світ. Поріг варіюється від 0 до QuantumRange і є мірою соляризації.

### Список параметрів

`threshold`

Ступінь соляризації.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
