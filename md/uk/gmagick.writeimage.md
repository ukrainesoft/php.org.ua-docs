---
navigation:
  - gmagick.write.md: '« Gmagick::write'
  - class.gmagickdraw.md: GmagickDraw »
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::writeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::writeimage

(PECL gmagick >= Unknown)

Gmagick::writeimage — Записує зображення у вказаний файл

### Опис

```methodsynopsis
public Gmagick::writeimage(string $filename, bool $all_frames = false): Gmagick
```

Записує зображення у вказаний файл. Якщо в якості імені файлу вказано **`null`**, то зображення буде записано у файл, заданий [Gmagick::readimage()](gmagick.readimage.md) або [Gmagick::setimagefilename()](gmagick.setimagefilename.md)

### Список параметрів

`filename`

Ім'я файлу.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
