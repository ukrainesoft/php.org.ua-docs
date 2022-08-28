Порівнює канали зображення з відновленим зображенням

-   [« Imagick::getImageChannelDepth](imagick.getimagechanneldepth.html)
    
-   [Imagick::getImageChannelDistortions »](imagick.getimagechanneldistortions.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Порівнює канали зображення з відновленим зображенням
    

# Imagick::getImageChannelDistortion

(PECL imagick 2, PECL imagick 3)

Imagick::getImageChannelDistortion — Порівнює канали зображення з відновленим зображенням

### Опис

```methodsynopsis
public Imagick::getImageChannelDistortion(Imagick $reference, int $channel, int $metric): float
```

Порівнює один або кілька каналів зображення з відновленим зображенням та повертає зазначений показник спотворення.

### Список параметрів

`reference`

Об'єкт Imagick для порівняння.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

`metric`

Одна з [констант типа METRIC](imagick.constants.html#imagick.constants.metric)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.