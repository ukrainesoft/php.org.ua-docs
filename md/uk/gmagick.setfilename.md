---
navigation:
  - gmagick.setcompressionquality.md: '« Gmagick::setCompressionQuality'
  - gmagick.setimagebackgroundcolor.md: 'Gmagick::setimagebackgroundcolor »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setfilename'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setfilename

(PECL gmagick >= Unknown)

Gmagick::setfilename — Встановлює ім'я файлу перед читанням або записуванням зображення

### Опис

```methodsynopsis
public Gmagick::setfilename(string $filename): Gmagick
```

Встановлює ім'я файлу перед читанням або записуванням зображення.

### Список параметрів

`filename`

Ім'я файлу.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
