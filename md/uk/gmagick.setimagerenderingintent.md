---
navigation:
  - gmagick.setimageredprimary.md: '« Gmagick::setimageredprimary'
  - gmagick.setimageresolution.md: 'Gmagick::setimageresolution »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagerenderingintent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Одна из констант[способу відображення](gmagick.constants.md#gmagick.constants.renderingintent) `Gmagick::RENDERINGINTENT_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
