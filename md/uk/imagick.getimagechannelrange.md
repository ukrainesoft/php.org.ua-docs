Повертає діапазон каналів

-   [« Imagick::getImageChannelMean](imagick.getimagechannelmean.html)
    
-   [Imagick::getImageChannelStatistics »](imagick.getimagechannelstatistics.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає діапазон каналів
    

# Imagick::getImageChannelRange

(PECL imagick 2> = 2.2.1, PECL imagick 3)

Imagick::getImageChannelRange — Повертає діапазон каналів

### Опис

```methodsynopsis
public Imagick::getImageChannelRange(int $channel): array
```

Повертає діапазон для одного або кількох каналів зображення. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.4.0 або старшим.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

Повертає масив, що містить мінімальні та максимальні значення каналу(ів).

### Помилки

Викликає ImagickException у разі виникнення помилки.