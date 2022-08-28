Приховує цифровий водяний знак у зображенні

-   [« Imagick::statisticImage](imagick.statisticimage.html)
    
-   [Imagick::stereoImage »](imagick.stereoimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Приховує цифровий водяний знак у зображенні
    

# Imagick::steganoImage

(PECL imagick 2, PECL imagick 3)

Imagick::steganoImage — Приховує цифровий водяний знак у зображенні

### Опис

```methodsynopsis
public Imagick::steganoImage(Imagick $watermark_wand, int $offset): Imagick
```

Приховує цифровий водяний знак у зображенні. Відновіть прихований водяний знак пізніше, щоб довести справжність зображення. Зсув визначає початкову позицію на зображенні, щоб приховати водяний знак.

### Список параметрів

`watermark_wand`

`offset`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**