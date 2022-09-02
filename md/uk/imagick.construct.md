---
navigation:
  - imagick.compositeimage.md: '« Imagick::compositeImage'
  - imagick.contrastimage.md: 'Imagick::contrastImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::construct'
---
# Imagick::construct

(PECL imagick 2, PECL imagick 3)

Imagick::construct — Конструктор об'єкту Imagick

### Опис

public **Imagick::construct**[mixed](language.types.declarations.md#language.types.declarations.mixed) `$files`

Створює екземпляр Imagick для окремого зображення чи групи зображень.

### Список параметрів

`files`

Шлях до зображення для завантаження чи масив таких шляхів. Шляхи можуть містити групові символи для імен файлів або можуть бути URL-адресою.

### Помилки

Викликає ImagickException у разі виникнення помилки.
