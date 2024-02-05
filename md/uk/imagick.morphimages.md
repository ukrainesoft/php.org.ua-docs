---
navigation:
  - imagick.montageimage.md: '« Imagick::montageImage'
  - imagick.morphology.md: 'Imagick::morphology »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::morphImages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::morphImages

(PECL imagick 2, PECL imagick 3)

Imagick::morphImages — Перетворює набір зображень

### Опис

```methodsynopsis
public Imagick::morphImages(int $number_frames): Imagick
```

Перетворює набір зображень. І пікселі зображення, і розмір лінійно інтерполуються, щоб створити видимість метаморфоз від одного зображення до іншого.

### Список параметрів

`number_frames`

Кількість проміжних зображень, що створюються.

### Значення, що повертаються

Метод повертає новий об'єкт Imagick у разі успішного виконання. Викликає **ImagickException**в случае возникновения ошибки.
