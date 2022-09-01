---
navigation:
  - gmagick.removeimage.md: '« Gmagick::removeimage'
  - gmagick.resampleimage.md: 'Gmagick::resampleimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::removeimageprofile'
---
# Gmagick::removeimageprofile

(PECL gmagick >= Unknown)

Gmagick::removeimageprofile — Видаляє іменований профайл зображення та повертає його

### Опис

```methodsynopsis
public Gmagick::removeimageprofile(string $name): string
```

Видаляє іменований профайл зображення та повертає його.

### Список параметрів

`name`

Ім'я профайлу: ICC, IPTC або базовий профайл.

### Значення, що повертаються

Іменований профайл.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
