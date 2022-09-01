---
navigation:
  - gmagick.setimageredprimary.html: '« Gmagick::setimageredprimary'
  - gmagick.setimageresolution.html: 'Gmagick::setimageresolution »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::setimagerenderingintent'
---
# Gmagick::setimagerenderingintent

(PECL gmagick >= Unknown)

Gmagick::setimagerenderingintent — Встановлює спосіб рендерингу зображення

### Опис

```methodsynopsis
public Gmagick::setimagerenderingintent(int $rendering_intent): Gmagick
```

Встановлює спосіб рендерингу зображення.

### Список параметрів

`rendering_intent`

Одна з констант [способа отображения](gmagick.constants.html#gmagick.constants.renderingintent) `Gmagick::RENDERINGINTENT_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
