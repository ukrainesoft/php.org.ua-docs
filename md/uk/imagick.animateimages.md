---
navigation:
  - imagick.affinetransformimage.md: '« Imagick::affineTransformImage'
  - imagick.annotateimage.md: 'Imagick::annotateImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::animateImages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::animateImages

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::animateImages — Анімація одного або кількох зображень

### Опис

```methodsynopsis
public Imagick::animateImages(string $x_server): bool
```

Метод здійснює анімацію зображення на локальному або віддаленому X сервері. Метод недоступний у Windows. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`x_server`

Адреса сервера X

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::displayImage()](imagick.displayimage.md) \- Виводить зображення
