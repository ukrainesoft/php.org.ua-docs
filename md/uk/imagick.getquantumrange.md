---
navigation:
  - imagick.getquantumdepth.md: '« Imagick::getQuantumDepth'
  - imagick.getregistry.md: 'Imagick::getRegistry »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getQuantumRange'
---
# Imagick::getQuantumRange

(PECL imagick 2, PECL imagick 3)

Imagick::getQuantumRange — Повертає розмір спектру Imagick

### Опис

```methodsynopsis
public static Imagick::getQuantumRange(): array
```

Повертає розмір розміру для об'єкта Imagick.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив, що містить розмір спектру як ціле число int (`"quantumRangeLong"`) і як рядок string (`"quantumRangeString"`

### Помилки

Викликає ImagickException у разі виникнення помилки.
