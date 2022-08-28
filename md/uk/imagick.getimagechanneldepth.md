Повертає глибину для певного каналу зображення

-   [« Imagick::getImageBorderColor](imagick.getimagebordercolor.html)
    
-   [Imagick::getImageChannelDistortion »](imagick.getimagechanneldistortion.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
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

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналов](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**