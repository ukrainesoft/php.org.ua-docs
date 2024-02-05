---
navigation:
  - imagick.convolveimage.md: '« Imagick::convolveImage'
  - imagick.cropimage.md: 'Imagick::cropImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::count

(PECL imagick 3 >= 3.3.0)

Imagick::count — Отримує кількість зображень

### Опис

```methodsynopsis
public Imagick::count(int $mode = 0): int
```

Повертає кількість зображень.

### Список параметрів

`mode`

Невикористовуваний аргумент. В даний час у PHP є не дуже чітко визначена функція, де виклик count() для лічильного об'єкта може (або не може) вимагати, щоб метод прийняв параметр. Параметр повинен відповідати інтерфейсу лічильного, навіть якщо він не використовується.

### Значення, що повертаються

Повертає кількість зображень.
