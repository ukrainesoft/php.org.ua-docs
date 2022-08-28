Відокремлює канал від зображення

-   [« Imagick::selectiveBlurImage](imagick.selectiveblurimage.html)
    
-   [Imagick::sepiaToneImage »](imagick.sepiatoneimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Відокремлює канал від зображення
    

# Imagick::separateImageChannel

(PECL imagick 2, PECL imagick 3)

Imagick::separateImageChannel — Відокремлює канал від зображення.

### Опис

```methodsynopsis
public Imagick::separateImageChannel(int $channel): bool
```

Відокремлює канал від зображення та повертає зображення у відтінках сірого. Канал – це певний колірний компонент кожного пікселя зображення.

### Список параметрів

`channel`

Визначає, який "канал" повернути. Для колірних просторів, відмінних від RGB, можна використовувати константи CHANNELRED, CHANNELGREEN, CHANNELBLUE для позначення 1-го, 2-го та 3-го каналів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::separateImageChannel()****

```php
<?php
function separateImageChannel($imagePath, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->separateimagechannel($channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

separateImageChannel($imagePath, \Imagick::CHANNEL_GREEN);

?>
```