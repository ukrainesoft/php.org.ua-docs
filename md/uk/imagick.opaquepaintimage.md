Змінює значення кольору будь-якого пікселя, що відповідає цільовому

-   [« Imagick::oilPaintImage](imagick.oilpaintimage.html)
    
-   [Imagick::optimizeImageLayers »](imagick.optimizeimagelayers.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Змінює значення кольору будь-якого пікселя, що відповідає цільовому
    

# Imagick::opaquePaintImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::opaquePaintImage — Змінює значення кольору будь-якого пікселя, що відповідає цільовому

### Опис

```methodsynopsis
public Imagick::opaquePaintImage(    mixed $target,    mixed $fill,    float $fuzz,    bool $invert,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює будь-який піксель, який відповідає кольору, на колір, визначений заливкою. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.8 або старшим.

### Список параметрів

`target`

Об'єкт ImagickPixel або рядок, який містить колір, який потрібно змінити

`fill`

Колір заміни

`fuzz`

міра округлення (fuzz). Для прикладу, встановіть значення fuzz 10 і червоний колір з інтенсивністю 100 і 102 буде інтерпретуватися як один і той же колір.

`invert`

Якщо **`true`** зафарбовується будь-який піксель, що не відповідає цільовому кольору.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналов](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**