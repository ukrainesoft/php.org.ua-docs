Змінює значення кольору будь-якого пікселя, що відповідає меті

-   [« Imagick::orderedPosterizeImage](imagick.orderedposterizeimage.html)
    
-   [Imagick::paintOpaqueImage »](imagick.paintopaqueimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Змінює значення кольору будь-якого пікселя, що відповідає меті
    

# Imagick::paintFloodfillImage

(PECL imagick 2> = 2.1.0, PECL imagick 3)

Imagick::paintFloodfillImage — Змінює значення кольору будь-якого пікселя, що відповідає меті

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::paintFloodfillImage(    mixed $fill,    float $fuzz,    mixed $bordercolor,    int $x,    int $y,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює значення кольору будь-якого пікселя, який відповідає цілі та є найближчим сусідом. Починаючи з ImageMagick 6.3.8, цей метод застарів і замість нього слід використовувати [Imagick::floodfillPaintImage()](imagick.floodfillpaintimage.html)

### Список параметрів

`fill`

Об'єкт ImagickPixel або рядок, який містить колір заливки.

`fuzz`

міра округлення (fuzz). Для прикладу, встановіть значення fuzz 10 і червоний колір з інтенсивністю 100 і 102 буде інтерпретуватися як один і той же колір.

`bordercolor`

Об'єкт ImagickPixel або рядок, який містить цільовий колір для малювання.

`x`

Початкова позиція заливки осі X.

`y`

Початкова позиція заливки осі Y.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**