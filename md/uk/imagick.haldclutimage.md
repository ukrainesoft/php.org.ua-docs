---
navigation:
  - imagick.getversion.md: '« Imagick::getVersion'
  - imagick.hasnextimage.md: 'Imagick::hasNextImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::haldClutImage'
---
# Imagick::haldClutImage

(PECL imagick 3)

Imagick::haldClutImage — Замінює кольори зображення.

### Опис

```methodsynopsis
public Imagick::haldClutImage(Imagick $clut, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Замінює кольори зображення за допомогою таблиці пошуку Hald. Hald-зображення можуть бути створені за допомогою колірного кодера HALD.

### Список параметрів

`clut`

Об'єкт Imagick, що містить пошукове зображення Hald.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::haldClutImage()****

```php
<?php
function haldClutImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagickPalette = new \Imagick(realpath("images/hald/hald_8.png"));
    $imagickPalette->sepiatoneImage(55);
    $imagick->haldClutImage($imagickPalette);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
