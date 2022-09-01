---
navigation:
  - imagick.getimagescene.md: '« Imagick::getImageScene'
  - imagick.getimagesize.md: 'Imagick::getImageSize »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageSignature'
---
# Imagick::getImageSignature

(PECL imagick 2, PECL imagick 3)

Imagick::getImageSignature - Генерує хеш SHA-256

### Опис

```methodsynopsis
public Imagick::getImageSignature(): string
```

Генерує хеш SHA-256 для потоку пікселів зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, який містить SHA-256 хеш файлу.

### Помилки

Викликає ImagickException у разі виникнення помилки.
