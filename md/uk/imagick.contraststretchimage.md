Підвищує контрастність кольорового зображення

-   [« Imagick::contrastImage](imagick.contrastimage.html)
    
-   [Imagick::convolveImage »](imagick.convolveimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Підвищує контрастність кольорового зображення
    

# Imagick::contrastStretchImage

(PECL imagick 2, PECL imagick 3)

Imagick::contrastStretchImage — Підвищує контрастність кольорового зображення

### Опис

```methodsynopsis
public Imagick::contrastStretchImage(float $black_point, float $white_point, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Підвищує контраст кольорового зображення, регулюючи колір пікселів для охоплення всього діапазону доступних кольорів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`black_point`

Чорна точка.

`white_point`

Білий крапку.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для застосування більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів . **`Imagick::CHANNEL_ALL`**. Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**