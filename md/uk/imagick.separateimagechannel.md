---
navigation:
  - imagick.selectiveblurimage.md: '« Imagick::selectiveBlurImage'
  - imagick.sepiatoneimage.md: 'Imagick::sepiaToneImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::separateImageChannel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Визначає, який 'канал' повернути. Для колірних просторів, відмінних від RGB, можна використовувати константи CHANNEL\_RED, CHANNEL\_GREEN, CHANNEL\_BLUE для позначення 1-го, 2-го та 3-го каналів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::separateImageChannel()\*\*\*\*

```php
<?php
function separateImageChannel($imagePath, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->separateimagechannel($channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

separateImageChannel($imagePath, \Imagick::CHANNEL_GREEN);

?>
```
