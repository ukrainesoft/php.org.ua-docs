---
navigation:
  - gmagick.construct.md: '« Gmagick::construct'
  - gmagick.cropthumbnailimage.md: 'Gmagick::cropthumbnailimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::cropimage'
---
# Gmagick::cropimage

(PECL gmagick >= Unknown)

Gmagick::cropimage — Обрізає зображення

### Опис

```methodsynopsis
public Gmagick::cropimage(    
    int
     $width
   ,    
    int
     $height
   ,    int $x,    int $y): Gmagick
```

Обрізає зображення.

### Список параметрів

`width`

Ширина ділянки, що зберігається.

`height`

Висота ділянки, що зберігається.

`x`

X координата лівого верхнього кута області, що зберігається.

`y`

Y координата лівого верхнього кута області, що зберігається.

### Значення, що повертаються

Обрізаний об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
