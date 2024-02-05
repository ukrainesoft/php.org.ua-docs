---
navigation:
  - gmagick.radialblurimage.md: '« Gmagick::radialblurimage'
  - gmagick.read.md: 'Gmagick::read »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::raiseimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::raiseimage

(PECL gmagick >= Unknown)

Gmagick::raiseimage — Створює імітацію ефекту тривимірної кнопки

### Опис

```methodsynopsis
public Gmagick::raiseimage(    int $width,    int $height,    int $x,    int $y,    bool $raise): Gmagick
```

Створює імітацію ефекту тривимірної кнопки, освітлюючи та затемнюючи краї зображення. Ширина та висота елементів raise\_info визначають ширину вертикального та горизонтального краю ефекту.

### Список параметрів

`width`

Ширина області, яку необхідно підняти.

`height`

Висота площі, що піднімається.

`x`

Координати X.

`y`

Координата Y.

`raise`

Значення, відмінне від нуля, створює ефект тривимірного підвищення, інакше - ефект зниження.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
