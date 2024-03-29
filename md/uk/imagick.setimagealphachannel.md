---
navigation:
  - imagick.setimage.md: '« Imagick::setImage'
  - imagick.setimageartifact.md: 'Imagick::setImageArtifact »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageAlphaChannel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageAlphaChannel

(PECL imagick 2 >= 2.1.0, PECL imagick 3)

Imagick::setImageAlphaChannel — Встановлює альфа-канал зображення

### Опис

```methodsynopsis
public Imagick::setImageAlphaChannel(int $mode): bool
```

Активує або деактивує альфа-канал зображення. Параметр `mode`\- одна из констант\*\*`Imagick::ALPHACHANNEL_*`\*\*. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.8 або старшим.

### Список параметрів

`mode`

Одна из констант\*\*`Imagick::ALPHACHANNEL_*`\*\*

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Дивіться також

-   [Imagick::setImageMatte()](imagick.setimagematte.md) \- Встановлює матовий канал зображення
-   [Константи альфа-каналу Imagick](imagick.constants.md#imagick.constants.alphachannel)
