---
navigation:
  - imagick.previousimage.md: '« Imagick::previousImage'
  - imagick.quantizeimage.md: 'Imagick::quantizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::profileImage'
---
# Imagick::profileImage

(PECL imagick 2, PECL imagick 3)

Imagick::profileImage — Додає або видаляє профіль зображення

### Опис

```methodsynopsis
public Imagick::profileImage(string $name, string $profile): bool
```

Додає або видаляє ICC, IPTC або загальний профіль зображення. Якщо профіль NULL, він видаляється, інакше додається. Використовуйте ім'я '' і профіль NULL, щоб видалити всі профілі зображення.

### Список параметрів

`name`

`profile`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
