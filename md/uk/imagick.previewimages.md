---
navigation:
  - imagick.posterizeimage.md: '« Imagick::posterizeImage'
  - imagick.previousimage.md: 'Imagick::previousImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::previewImages'
---
# Imagick::previewImages

(PECL imagick 2, PECL imagick 3)

Imagick::previewImages — Швидке визначення відповідних параметрів для обробки зображень

### Опис

```methodsynopsis
public Imagick::previewImages(int $preview): bool
```

Розміщує 9 мініатюр вказаного зображення за допомогою операції обробки зображення, що застосовується з різною інтенсивністю. Це допомагає швидко визначити відповідний параметр для обробки зображення.

### Список параметрів

`preview`

Тип попереднього перегляду. Дивіться [константи типу попереднього перегляду](imagick.constants.md#imagick.constants.preview)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
