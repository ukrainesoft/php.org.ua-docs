---
navigation:
  - imagick.coalesceimages.md: '« Imagick::coalesceImages'
  - imagick.colorizeimage.md: 'Imagick::colorizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::colorFloodfillImage'
---
# Imagick::colorFloodfillImage

(PECL imagick 2, PECL imagick 3)

Imagick::colorFloodfillImage — Змінює значення кольору будь-якого пікселя, що відповідає цільовому

**Увага**

Функція оголошена *Застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::colorFloodfillImage(    mixed $fill,    float $fuzz,    mixed $bordercolor,    int $x,    int $y): bool
```

Змінює значення кольору будь-якого пікселя, що відповідає цільовому та є найближчим сусідом.

### Список параметрів

`fill`

Об'єкт ImagickPixel, що містить колір заливки.

`fuzz`

міра округлення (fuzz). Наприклад, надайте fuzz значення, що дорівнює 10, і червоний колір з інтенсивністю 100 і 102 відповідно тепер інтерпретуватиметься як один і той же колір для цілей заливання.

`bordercolor`

Об'єкт ImagickPixel, що містить колір кордону.

`x`

Початкова позиція заливки X.

`y`

Початкова позиція заливання Y.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як перший і третій параметрів. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |
