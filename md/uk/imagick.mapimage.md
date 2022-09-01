---
navigation:
  - imagick.magnifyimage.md: '« Imagick::magnifyImage'
  - imagick.mattefloodfillimage.md: 'Imagick::matteFloodfillImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::mapImage'
---
# Imagick::mapImage

(PECL imagick 2, PECL imagick 3)

Imagick::mapImage — Замінює кольори зображення на найближчий колір із еталонного зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::mapImage(Imagick $map, bool $dither): bool
```

### Список параметрів

`map`

`dither`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
