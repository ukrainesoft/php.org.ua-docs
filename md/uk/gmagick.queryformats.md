---
navigation:
  - gmagick.queryfonts.md: '« Gmagick::queryfonts'
  - gmagick.radialblurimage.md: 'Gmagick::radialblurimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::queryformats'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
