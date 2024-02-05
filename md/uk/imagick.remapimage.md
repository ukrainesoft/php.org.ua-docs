---
navigation:
  - imagick.reducenoiseimage.md: '« Imagick::reduceNoiseImage'
  - imagick.removeimage.md: 'Imagick::removeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::remapImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::remapImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::remapImage — Визначає кольори зображення.

### Опис

```methodsynopsis
public Imagick::remapImage(Imagick $replacement, int $DITHER): bool
```

Замінює кольори зображення на ті, які визначені параметром `replacement`. Кольори замінюються найближчим із можливих. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.5 або старшим.

### Список параметрів

`replacement`

Об'єкт Imagick, що містить кольори, що замінюють.

`DITHER`

Обратитесь к списку[констант DITHERMETHOD](imagick.constants.md#imagick.constants.dithermethod)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
