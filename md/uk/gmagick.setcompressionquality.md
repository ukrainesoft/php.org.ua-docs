---
navigation:
  - gmagick.separateimagechannel.md: '« Gmagick::separateimagechannel'
  - gmagick.setfilename.md: 'Gmagick::setfilename »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setCompressionQuality'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setCompressionQuality

(No version information available, might only be in Git)

Gmagick::setCompressionQuality — Встановлює якість стандартного стиснення об'єкта.

### Опис

```methodsynopsis
Gmagick::setCompressionQuality(
    int $quality
     = 75
   ): Gmagick
```

Встановлює якість стандартного стиснення об'єкта.

### Список параметрів

`quality`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Gmagick::setCompressionQuality()\*\*\*\*

```php
<?php
$gm = new Gmagick();
$gm->read("magick:rose");
$gm->setCompressionQuality(2);
?>
```
