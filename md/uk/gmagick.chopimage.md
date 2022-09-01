---
navigation:
  - gmagick.charcoalimage.html: '« Gmagick::charcoalimage'
  - gmagick.clear.html: 'Gmagick::clear »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::chopimage'
---
# Gmagick::chopimage

(PECL gmagick >= Unknown)

Gmagick::chopimage — Видаляє область зображення та підрізає його.

### Опис

```methodsynopsis
public Gmagick::chopimage(    int $width,    int $height,    int $x,    int $y): Gmagick
```

Видаляє область зображення та плескає його так, щоб зайняти віддалену область.

### Список параметрів

`width`

Ширина ділянки, що вирізається.

`height`

Висота ділянки, що вирізується.

`x`

Горизонтальне усунення початку вирізки.

`y`

Вертикальне усунення початку вирізки.

### Значення, що повертаються

Об'єкт, що вийшов [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
