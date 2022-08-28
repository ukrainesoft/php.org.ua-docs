Застосовує вираз до зображення

-   [« Imagick::equalizeImage](imagick.equalizeimage.html)
    
-   [Imagick::exportImagePixels »](imagick.exportimagepixels.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Застосовує вираз до зображення
    

# Imagick::evaluateImage

(PECL imagick 2, PECL imagick 3)

Imagick::evaluateImage — Застосовує вираз до зображення

### Опис

```methodsynopsis
public Imagick::evaluateImage(int $op, float $constant, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує зображення арифметичне, реляційне або логічне вираз. Використовуйте ці оператори для освітлення або затемнення зображення, збільшення або зменшення контрастності зображення або створення "негативу" зображення.

### Список параметрів

`op`

Оператор обчислення.

`constant`

Значення оператора.

`channel`

Вкажіть будь-яку константу CHANNEL, яка підходить для вашого режиму каналу. Для використання більш ніж одного каналу об'єднайте константи типу CHANNEL за допомогою побітових операторів.Зверніться до цього списку [констант CHANNEL](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::evaluateImage()****

Використання evaluateImage для зменшення непрозорості зображення.

```php
<?php
// Создание нового объекта с изображением
$im = new Imagick('example-alpha.png');

// Уменьшение значнения альфа-канала на 50%
$im->evaluateImage(Imagick::EVALUATE_DIVIDE, 2, Imagick::CHANNEL_ALPHA);

// Вывод изображения
header("Content-Type: image/png");
echo $im;
?>
```