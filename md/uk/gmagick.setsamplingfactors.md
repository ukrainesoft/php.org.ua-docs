---
navigation:
  - gmagick.setimagewhitepoint.md: '« Gmagick::setimagewhitepoint'
  - gmagick.setsize.md: 'Gmagick::setsize »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setsamplingfactors'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setsamplingfactors

(PECL gmagick >= Unknown)

Gmagick::setsamplingfactors — Встановлює фактори вибірки зображення

### Опис

```methodsynopsis
public Gmagick::setsamplingfactors(array $factors): Gmagick
```

Встановлює фактори вибірки зображення.

### Список параметрів

`factors`

Масив значень з типом float, що є фактором вибірки для кожного компонента кольору (у порядку RGB).

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
