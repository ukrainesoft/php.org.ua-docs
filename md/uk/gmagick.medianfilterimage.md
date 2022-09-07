---
navigation:
  - gmagick.mapimage.md: '« Gmagick::mapimage'
  - gmagick.minifyimage.md: 'Gmagick::minifyimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::medianfilterimage'
---
# Gmagick::medianfilterimage

(PECL gmagick >= Unknown)

Gmagick::medianfilterimage — Застосовує цифровий фільтр

### Опис

```methodsynopsis
public Gmagick::medianfilterimage(float $radius): void
```

Застосовує цифровий фільтр, який покращує якість зашумленого зображення. Кожен піксель замінюється медіаною у наборі сусідніх пікселів, що визначаються радіусом.

### Список параметрів

`radius`

Радіус околиці пікселів.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) із застосованим медіанним фільтром.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
