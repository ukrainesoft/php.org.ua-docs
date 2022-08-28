Повертає спотворення каналу

-   [« Imagick::getImageChannelDistortion](imagick.getimagechanneldistortion.html)
    
-   [Imagick::getImageChannelExtrema »](imagick.getimagechannelextrema.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає спотворення каналу
    

# Imagick::getImageChannelDistortions

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::getImageChannelDistortions — Повертає спотворення каналу

### Опис

```methodsynopsis
public Imagick::getImageChannelDistortions(Imagick $reference, int $metric, int $channel = Imagick::CHANNEL_DEFAULT): float
```

Порівнює один або кілька каналів зображення з відновленим зображенням та повертає зазначений показник спотворення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.4 або старшим.

### Список параметрів

`reference`

Об'єкт Imagick, що містить зображення, з яким проводиться порівняння.

`metric`

Зверніться до цього списку [констант типа METRIC](imagick.constants.html#imagick.constants.metric)

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналов](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

Повертає число з плаваючою точкою, що описує спотворення каналу.

### Помилки

Викликає ImagickException у разі виникнення помилки.