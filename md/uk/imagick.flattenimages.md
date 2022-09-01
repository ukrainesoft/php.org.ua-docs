---
navigation:
  - imagick.filter.md: '« Imagick::filter'
  - imagick.flipimage.md: 'Imagick::flipImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::flattenImages'
---
# Imagick::flattenImages

(PECL imagick 2, PECL imagick 3)

Imagick::flattenImages — Об'єднує послідовність зображень

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::flattenImages(): Imagick
```

Поєднує послідовність зображень. Корисно для поєднання шарів Photoshop в одне зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
