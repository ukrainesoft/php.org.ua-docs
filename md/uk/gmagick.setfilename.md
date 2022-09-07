---
navigation:
  - gmagick.setcompressionquality.md: '« Gmagick::setCompressionQuality'
  - gmagick.setimagebackgroundcolor.md: 'Gmagick::setimagebackgroundcolor »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setfilename'
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

Викликає **GmagickException** у разі виникнення помилки.
