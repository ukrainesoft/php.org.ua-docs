---
navigation:
  - gmagick.swirlimage.md: '« Gmagick::swirlimage'
  - gmagick.trimimage.md: 'Gmagick::trimimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::thumbnailimage'
---
# Gmagick::thumbnailimage

(PECL gmagick >= Unknown)

Gmagick::thumbnailimage — Змінює розмір зображення

### Опис

```methodsynopsis
public Gmagick::thumbnailimage(int $width, int $height, bool $fit = false): Gmagick
```

Змінює розмір зображення до заданих розмірів та видаляє пов'язані профілі. Мета полягає у створенні невеликих мініатюрних зображень, які підходять для показу в Інтернеті. Якщо в якості третього параметра встановлено значення **`true`**, то параметри стовпців і рядків використовуються як максимуми для кожної сторони. Обидві сторони будуть зменшені до збігу або менше параметра, заданого для сторони.

### Список параметрів

`width`

Ширина зображення.

`height`

Висота зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
