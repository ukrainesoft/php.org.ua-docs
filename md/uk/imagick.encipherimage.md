---
navigation:
  - imagick.embossimage.md: '« Imagick::embossImage'
  - imagick.enhanceimage.md: 'Imagick::enhanceImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::encipherImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::encipherImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::encipherImage — Шифрує зображення

### Опис

```methodsynopsis
public Imagick::encipherImage(string $passphrase): bool
```

Перетворює звичайні пікселі на зашифровані пікселі. Зображення не читається, доки не буде розшифровано функцією [Imagick::decipherImage()](imagick.decipherimage.md) Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`passphrase`

Пароль

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::decipherImage()](imagick.decipherimage.md) \- Розшифровує зображення
