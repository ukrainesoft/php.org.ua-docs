Встановлює якість стандартного стиснення об'єкта

-   [« Gmagick::separateimagechannel](gmagick.separateimagechannel.html)
    
-   [Gmagick::setfilename »](gmagick.setfilename.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Встановлює якість стандартного стиснення об'єкта
    

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

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Gmagick::setCompressionQuality()****

```php
<?php
$gm = new Gmagick();
$gm->read("magick:rose");
$gm->setCompressionQuality(2);
?>
```