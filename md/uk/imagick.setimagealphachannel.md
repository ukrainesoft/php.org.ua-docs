Встановлює альфа-канал зображення

-   [« Imagick::setImage](imagick.setimage.html)
    
-   [Imagick::setImageArtifact »](imagick.setimageartifact.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює альфа-канал зображення
    

# Imagick::setImageAlphaChannel

(PECL imagick 2> = 2.1.0, PECL imagick 3)

Imagick::setImageAlphaChannel — Встановлює альфа-канал зображення

### Опис

```methodsynopsis
public Imagick::setImageAlphaChannel(int $mode): bool
```

Активує або деактивує альфа-канал зображення. Параметр `mode` - одна з констант **`Imagick::ALPHACHANNEL_*`**. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.8 або старшим.

### Список параметрів

`mode`

Одна з констант **`Imagick::ALPHACHANNEL_*`**

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Дивіться також

-   [Imagick::setImageMatte()](imagick.setimagematte.html) - Встановлює матовий канал зображення
-   [Константы альфа-канала Imagick](imagick.constants.html#imagick.constants.alphachannel)