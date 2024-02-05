---
navigation:
  - imagick.roundcorners.md: '« Imagick::roundCorners'
  - imagick.scaleimage.md: 'Imagick::scaleImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::sampleImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::sampleImage

(PECL imagick 2, PECL imagick 3)

Imagick::sampleImage — Масштабує зображення з піксельною вибіркою

### Опис

```methodsynopsis
public Imagick::sampleImage(int $columns, int $rows): bool
```

Масштабує зображення до бажаних розмірів за допомогою вибірки пікселів. На відміну від інших методів масштабування, цей метод не вводить додатковий колір масштабованого зображення.

### Список параметрів

`columns`

`rows`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
