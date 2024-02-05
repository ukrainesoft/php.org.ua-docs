---
navigation:
  - imagick.chopimage.md: '« Imagick::chopImage'
  - imagick.clear.md: 'Imagick::clear »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::clampImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::clampImage

(PECL imagick 3 >= 3.3.0)

Imagick::clampImage — Обмежує діапазон кольорів від 0 до квантової глибини.

### Опис

```methodsynopsis
public Imagick::clampImage(int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Обмежує діапазон кольорів від 0 до квантової глибини.

### Список параметрів

`channel`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
