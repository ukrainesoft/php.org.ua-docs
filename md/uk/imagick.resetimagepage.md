---
navigation:
  - imagick.resampleimage.md: '« Imagick::resampleImage'
  - imagick.resizeimage.md: 'Imagick::resizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::resetImagePage'
---
# Imagick::resetImagePage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::resetImagePage — Скидає сторінку зображення

### Опис

```methodsynopsis
public Imagick::resetImagePage(string $page): bool
```

Визначення сторінки у вигляді рядка. Рядок має формат WxH+x+y. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`page`

Визначення сторінки. Наприклад, `7168x5147+0+0`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
