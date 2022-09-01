---
navigation:
  - imagick.roundcorners.html: '« Imagick::roundCorners'
  - imagick.scaleimage.html: 'Imagick::scaleImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::sampleImage'
---
# Imagick::sampleImage

(PECL imagick 2, PECL imagick 3)

Imagick::sampleImage — Масштабує зображення з піксельною вибіркою

### Опис

```methodsynopsis
public Imagick::sampleImage(int $columns, int $rows): bool
```

Масштабує зображення до бажаних розмірів за допомогою вибірки пікселів. На відміну від інших методів масштабування, цей метод не вводить додатковий колір у масштабоване зображення.

### Список параметрів

`columns`

`rows`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
