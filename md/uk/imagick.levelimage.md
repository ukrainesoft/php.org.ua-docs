Регулює рівні зображення

-   [« Imagick::labelImage](imagick.labelimage.html)
    
-   [Imagick::linearStretchImage »](imagick.linearstretchimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Регулює рівні зображення
    

# Imagick::levelImage

(PECL imagick 2, PECL imagick 3)

Imagick::levelImage — Регулює рівні зображення

### Опис

```methodsynopsis
public Imagick::levelImage(    float $blackPoint,    float $gamma,    float $whitePoint,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Регулює рівні зображення, масштабуючи кольори, що потрапляють між зазначеними білими та чорними точками, до доступного квантового діапазону. Надані параметри є чорними, середніми і білими точками. Чорна точка визначає темний колір зображення. Кольори темніші за крапку чорного встановлюються на нуль. Середня точка визначає гамма-корекцію, що застосовується до зображення. Біла точка визначає найсвітліший колір зображення. Для кольорів яскравіше крапки білого встановлюється максимальне квантове значення.

### Список параметрів

`blackPoint`

Чорна точка зображення.

`gamma`

Значення гами.

`whitePoint`

Білий точки зображення.

`channel`

Вкажіть будь-яку константу каналу, яка відповідає режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до цього списку [констант канала](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::levelImage()****

```php
<?php
function levelImage($blackPoint, $gamma, $whitePoint) {
    $imagick = new \Imagick();
    $imagick->newPseudoimage(500, 500, 'gradient:black-white');

    $imagick->setFormat('png');
    $quantum = $imagick->getQuantum();
    $imagick->levelImage($blackPoint / 100 , $gamma, $quantum * $whitePoint / 100);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```