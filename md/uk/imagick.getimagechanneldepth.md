Повертає глибину для певного каналу зображення

-   [« Imagick::getImageBorderColor](imagick.getimagebordercolor.md)
    
-   [Imagick::getImageChannelDistortion »](imagick.getimagechanneldistortion.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Повертає глибину для певного каналу зображення
    

# Imagick::getImageChannelDepth

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelDepth — Повертає глибину для певного каналу зображення

### Опис

```methodsynopsis
public Imagick::getImageChannelDepth(int $channel): int
```

Повертає глибину для певного каналу зображення.

### Список параметрів

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**