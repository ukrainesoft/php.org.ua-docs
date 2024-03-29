---
navigation:
  - imagick.paintopaqueimage.md: '« Imagick::paintOpaqueImage'
  - imagick.pingimage.md: 'Imagick::pingImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::paintTransparentImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::paintTransparentImage

(PECL imagick 2, PECL imagick 3)

Imagick::paintTransparentImage — Змінює будь-який піксель, що відповідає кольору, на колір, визначений заливкою

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::paintTransparentImage(mixed $target, float $alpha, float $fuzz): bool
```

Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою.

### Список параметрів

`target`

Цільовий колір, що замінюється на вказане значення непрозорості зображення.

`alpha`

Рівень прозорості: 1.0 – повністю непрозорий, 0.0 – повністю прозорий.

`fuzz`

Визначає, наскільки можна вважати два кольори однаковими.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як перший параметр. Попередні версії допускали лише об'єкт ImagickPixel. |
