---
navigation:
  - imagick.borderimage.md: '« Imagick::borderImage'
  - imagick.charcoalimage.md: 'Imagick::charcoalImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::brightnessContrastImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::brightnessContrastImage

(PECL imagick 3 >= 3.3.0)

Imagick::brightnessContrastImage — Змінює яскравість та/або контраст зображення

### Опис

```methodsynopsis
public Imagick::brightnessContrastImage(float $brightness, float $contrast, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює яскравість та/або контраст зображення. Перетворює параметри яскравості та контрастності в нахил та перетин та викликає поліномічну функцію для застосування до зображення.

### Список параметрів

`brightness`

`contrast`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад использования метода**Imagick::brightnessContrastImage()\*\*\*\*

```php
<?php
function brightnessContrastImage($imagePath, $brightness, $contrast, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->brightnessContrastImage($brightness, $contrast, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
