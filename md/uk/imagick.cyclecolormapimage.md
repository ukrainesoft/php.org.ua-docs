---
navigation:
  - imagick.current.md: '« Imagick::current'
  - imagick.decipherimage.md: 'Imagick::decipherImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::cycleColormapImage'
---
# Imagick::cycleColormapImage

(PECL imagick 2, PECL imagick 3)

Imagick::cycleColormapImage — Відображає колірну карту зображення

### Опис

```methodsynopsis
public Imagick::cycleColormapImage(int $displace): bool
```

Зміщує колірну карту зображення на задану кількість позицій. Якщо ви циклічно змінюєте картку кольорів кілька разів, ви можете зробити психоделічний ефект.

### Список параметрів

`displace`

Кількість для усунення колірної карти.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
