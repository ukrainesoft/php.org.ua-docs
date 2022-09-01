---
navigation:
  - imagick.fximage.md: '« Imagick::fxImage'
  - imagick.gaussianblurimage.md: 'Imagick::gaussianBlurImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::gammaImage'
---
# Imagick::gammaImage

(PECL imagick 2, PECL imagick 3)

Imagick::gammaImage — Гамма-корекція зображення

### Опис

```methodsynopsis
public Imagick::gammaImage(float $gamma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Гамма-корекція зображення. Одне й те зображення, що переглядається різних пристроях, буде різнитися у сприйнятті, у способі представлення інтенсивності зображення на екрані. Вкажіть індивідуальні рівні гами для червоного, зеленого та синього каналів або налаштуйте всі три за допомогою параметра гами. Зазвичай, значення варіюються від 0.8 до 2.3.

### Список параметрів

`gamma`

Величина гамма-корекції.

`channel`

Вкажіть будь-яку константу каналу, яка відповідає режиму каналу. Щоб застосувати більше одного каналу, об'єднайте константи типу каналу за допомогою побітових операторів. Зверніться до цього списку [констант канала](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::gammaImage()****

```php
<?php
function gammaImage($imagePath, $gamma, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->gammaImage($gamma, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
