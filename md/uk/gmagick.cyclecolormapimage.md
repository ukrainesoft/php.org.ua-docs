---
navigation:
  - gmagick.current.md: '« Gmagick::current'
  - gmagick.deconstructimages.md: 'Gmagick::deconstructimages »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::cyclecolormapimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::cyclecolormapimage

(PECL gmagick >= Unknown)

Gmagick::cyclecolormapimage — Зміщує колірну карту зображення

### Опис

```methodsynopsis
public Gmagick::cyclecolormapimage(int $displace): Gmagick
```

Зміщує колірну карту зображення на задану кількість позицій. Якщо ви циклічно змінюєте картку кольорів кілька разів, ви можете зробити психоделічний ефект.

### Список параметрів

`displace`

Кількість зсувів карти кольорів.

### Значення, що повертаються

Повертає себе у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
