Повертає різницю в одному або кількох зображеннях

-   [« Imagick::commentImage](imagick.commentimage.md)
    
-   [Imagick::compareImageLayers »](imagick.compareimagelayers.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Повертає різницю в одному або кількох зображеннях
    

# Imagick::compareImageChannels

(PECL imagick 2, PECL imagick 3)

Imagick::compareImageChannels — Повертає різницю в одному або кількох зображеннях

### Опис

```methodsynopsis
public Imagick::compareImageChannels(Imagick $image, int $channelType, int $metricType): array
```

Порівнює одне або кілька зображень та повертає різницеве ​​зображення.

### Список параметрів

`image`

Об'єкт Imagick, що містить зображення для порівняння.

`channelType`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

`metricType`

Одна з [констант типа METRIC](imagick.constants.html#imagick.constants.metric)

### Значення, що повертаються

Масив, що складається з `new_wand` і `distortion`

### Помилки

Викликає ImagickException у разі виникнення помилки.