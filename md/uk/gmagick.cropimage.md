---
navigation:
  - gmagick.construct.md: '« Gmagick::\_\_construct'
  - gmagick.cropthumbnailimage.md: 'Gmagick::cropthumbnailimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::cropimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
