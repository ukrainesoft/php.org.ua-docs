---
navigation:
  - gmagick.edgeimage.md: '« Gmagick::edgeimage'
  - gmagick.enhanceimage.md: 'Gmagick::enhanceimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::embossimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::embossimage

(PECL gmagick >= Unknown)

Gmagick::embossimage — Повертає зображення у градаціях сірого з тривимірним ефектом

### Опис

```methodsynopsis
public Gmagick::embossimage(float $radius, float $sigma): Gmagick
```

Повертає зображення у градаціях сірого із тривимірним ефектом. Ми згортаємо зображення за допомогою гаусівського оператора, заданого радіусу та стандартного відхилення (сигма). Для отримання розумних результатів радіус має бути більшим за сигму. При використанні радіуса 0, радіус вибереться автоматично.

### Список параметрів

`radius`

Радіус ефекту.

`sigma`

Сигма ефект.

### Значення, що повертаються

Рельєфний об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
