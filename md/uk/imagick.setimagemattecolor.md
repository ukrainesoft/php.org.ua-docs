---
navigation:
  - imagick.setimagematte.md: '« Imagick::setImageMatte'
  - imagick.setimageopacity.md: 'Imagick::setImageOpacity »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageMatteColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageMatteColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageMatteColor — Встановлює матовий колір зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::setImageMatteColor(mixed $matte): bool
```

Встановлює матовий колір зображення.

### Список параметрів

`matte`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як параметр. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |
