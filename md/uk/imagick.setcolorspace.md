Встановлює колірний простір

-   [« Imagick::setBackgroundColor](imagick.setbackgroundcolor.html)
    
-   [Imagick::setCompression »](imagick.setcompression.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює колірний простір
    

# Imagick::setColorspace

(PECL imagick 3)

Imagick::setColorspace — Встановлює колірний простір

### Опис

```methodsynopsis
public Imagick::setColorspace(int $COLORSPACE): bool
```

Встановлює значення глобального кольору для об'єкта. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.5.7 або старшим.

### Список параметрів

`COLORSPACE`

Одна з [констант COLORSPACE](imagick.constants.html#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.