---
navigation:
  - imagick.cyclecolormapimage.md: '« Imagick::cycleColormapImage'
  - imagick.deconstructimages.md: 'Imagick::deconstructImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::decipherImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::decipherImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::decipherImage — Розшифровує зображення

### Опис

```methodsynopsis
public Imagick::decipherImage(string $passphrase): bool
```

Розшифровує зображення, яке було раніше зашифровано. Зображення має бути зашифроване з використанням [Imagick::encipherImage()](imagick.encipherimage.md). Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`passphrase`

Пароль

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::encipherImage()](imagick.encipherimage.md) \- Шифрує зображення
