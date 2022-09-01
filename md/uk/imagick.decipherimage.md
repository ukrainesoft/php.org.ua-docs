---
navigation:
  - imagick.cyclecolormapimage.html: '« Imagick::cycleColormapImage'
  - imagick.deconstructimages.html: 'Imagick::deconstructImages »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::decipherImage'
---
# Imagick::decipherImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::decipherImage — Розшифровує зображення

### Опис

```methodsynopsis
public Imagick::decipherImage(string $passphrase): bool
```

Розшифровує зображення, яке було зашифровано раніше. Зображення має бути зашифроване з використанням [Imagick::encipherImage()](imagick.encipherimage.html). Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`passphrase`

Пароль

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::encipherImage()](imagick.encipherimage.html) - Шифрує зображення
