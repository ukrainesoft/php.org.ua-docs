---
navigation:
  - gmagick.queryfonts.md: '« Gmagick::queryfonts'
  - gmagick.radialblurimage.md: 'Gmagick::radialblurimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::queryformats'
---
# Gmagick::queryformats

(PECL gmagick >= Unknown)

Gmagick::queryformats — Повертає формати, які підтримує Gmagick

### Опис

```methodsynopsis
public Gmagick::queryformats(string $pattern = "*"): array
```

Повертає формати, що підтримуються [Gmagick](class.gmagick.md)

### Список параметрів

`pattern`

Задає рядок (string), що містить шаблон.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
