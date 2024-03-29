---
navigation:
  - imagick.mapimage.md: '« Imagick::mapImage'
  - imagick.medianfilterimage.md: 'Imagick::medianFilterImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::matteFloodfillImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::matteFloodfillImage

(PECL imagick 2, PECL imagick 3)

Imagick::matteFloodfillImage — Змінює значення прозорості кольору

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::matteFloodfillImage(    float $alpha,    float $fuzz,    mixed $bordercolor,    int $x,    int $y): bool
```

Змінює значення прозорості будь-якого пікселя, що відповідає меті та є найближчим сусідом. Якщо вказано метод **`FillToBorderMethod`**, значення прозорості змінюється для будь-якого сусіднього пікселя, який не відповідає елементу bordercolor зображення.

### Список параметрів

`alpha`

Рівень прозорості: 1.0 – повністю непрозорий, а 0.0 – повністю прозорий.

`fuzz`

Елемент fuzz зображення визначає, наскільки можна вважати два кольори однаковими.

`bordercolor`

Об'єкт [ImagickPixel](class.imagickpixel.md) або рядок, що представляє колір кадру.

`x`

Початкова координата X операції.

`y`

Початкова координата Y операції.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє рядок, що представляє колір, як третій параметр. Попередні версії допускали лише об'єкт [ImagickPixel](class.imagickpixel.md) |
