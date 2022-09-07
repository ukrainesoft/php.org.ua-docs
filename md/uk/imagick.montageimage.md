---
navigation:
  - imagick.modulateimage.md: '« Imagick::modulateImage'
  - imagick.morphimages.md: 'Imagick::morphImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::montageImage'
---
# Imagick::montageImage

(PECL imagick 2, PECL imagick 3)

Imagick::montageImage — Створює складне зображення

### Опис

```methodsynopsis
public Imagick::montageImage(    ImagickDraw $draw,    string $tile_geometry,    string $thumbnail_geometry,    int $mode,    string $frame): Imagick
```

Створює складне зображення шляхом поєднання кількох окремих зображень. Зображення розміщуються на складовому зображенні мозаїкою, ім'я зображення може відображатися відразу під окремою плиткою.

### Список параметрів

`draw`

Назва, розмір та колір шрифту беруться з цього об'єкта.

`tile_geometry`

Кількість плиток у рядку та на сторінці (наприклад, 6x4+0+0).

`thumbnail_geometry`

Переважний розмір зображення та розмір кожної мініатюри (наприклад, 120x120+4+3).

`mode`

Режим кадрування мініатюр, дивіться [константи режиму кадрування](imagick.constants.md#imagick.constants.montagemode)

`frame`

Обведіть зображення декоративною рамкою (наприклад, 15x15+3+3). Колір рамки відповідає матовому кольору ескізу.

### Значення, що повертаються

Створює складне зображення та повертає його як новий об'єкт [Imagick](class.imagick.md)
