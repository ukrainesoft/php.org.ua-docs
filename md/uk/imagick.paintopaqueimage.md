---
navigation:
  - imagick.paintfloodfillimage.md: '« Imagick::paintFloodfillImage'
  - imagick.painttransparentimage.md: 'Imagick::paintTransparentImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::paintOpaqueImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::paintOpaqueImage

(PECL imagick 2, PECL imagick 3)

Imagick::paintOpaqueImage — Змінює будь-який піксель, що відповідає кольору

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::paintOpaqueImage(    mixed $target,    mixed $fill,    float $fuzz,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою.

### Список параметрів

`target`

Змінює цільовий колір на колір заливки зображення. Об'єкт ImagickPixel або рядок, який представляє цільовий колір.

`fill`

Об'єкт ImagickPixel або рядок, який представляє колір заливки.

`fuzz`

Міра округлення (fuzz) зображення визначає, наскільки прийнятно розглядати два кольори як і той самий.

`channel`

Вкажіть будь-яку константу каналу, яка відповідає режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до цього списку [констант каналу](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер допускається передавати рядок, що представляє колір, перший і другий параметр. Попередні версії допускали лише об'єкт ImagickPixel. |
