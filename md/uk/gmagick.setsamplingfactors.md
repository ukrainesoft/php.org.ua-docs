---
navigation:
  - gmagick.setimagewhitepoint.md: '« Gmagick::setimagewhitepoint'
  - gmagick.setsize.md: 'Gmagick::setsize »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setsamplingfactors'
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

Масив значень типу double, що представляє фактор вибірки кожного компонента кольору (у порядку RGB).

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
