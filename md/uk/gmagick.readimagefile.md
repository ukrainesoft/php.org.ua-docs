---
navigation:
  - gmagick.readimageblob.md: '« Gmagick::readimageblob'
  - gmagick.reducenoiseimage.md: 'Gmagick::reducenoiseimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::readimagefile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::readimagefile

(PECL gmagick >= Unknown)

Gmagick::readimagefile — Читає зображення або послідовність зображень із файлового дескриптора

### Опис

```methodsynopsis
public Gmagick::readimagefile(resource $fp, string $filename = ?): Gmagick
```

Читає зображення або послідовність зображень із файлового дескриптора.

### Список параметрів

`fp`

Дескриптор файлу.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
