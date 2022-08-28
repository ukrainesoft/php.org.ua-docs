Повертає ексцес та асиметрію певного каналу

-   [« Imagick::getImageChannelExtrema](imagick.getimagechannelextrema.html)
    
-   [Imagick::getImageChannelMean »](imagick.getimagechannelmean.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає ексцес та асиметрію певного каналу
    

# Imagick::getImageChannelKurtosis

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::getImageChannelKurtosis — Повертає ексцес та асиметрію певного каналу

### Опис

```methodsynopsis
public Imagick::getImageChannelKurtosis(int $channel = Imagick::CHANNEL_DEFAULT): array
```

Повертає ексцес та асиметрію певного каналу. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.9 або старшим.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналов](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

Повертає масив із елементами `kurtosis` і `skewness`

### Помилки

Викликає ImagickException у разі виникнення помилки.