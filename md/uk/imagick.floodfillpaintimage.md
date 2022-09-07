---
navigation:
  - imagick.flipimage.md: '« Imagick::flipImage'
  - imagick.flopimage.md: 'Imagick::flopImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::floodFillPaintImage'
---
# Imagick::floodFillPaintImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::floodFillPaintImage — Змінює значення кольору будь-якого пікселя, що відповідає цільовому

### Опис

```methodsynopsis
public Imagick::floodFillPaintImage(    mixed $fill,    float $fuzz,    mixed $target,    int $x,    int $y,    bool $invert,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Змінює значення кольору будь-якого пікселя, що відповідає цільовому та є найближчим сусідом. Даний метод – заміна застарілому [Imagick::paintFloodFillImage()](imagick.paintfloodfillimage.md). Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.8 або старшим.

### Список параметрів

`fill`

Об'єкт ImagickPixel або рядок, який містить колір заливки.

`fuzz`

міра округлення (fuzz). Для прикладу, встановіть значення fuzz 10 і червоний колір з інтенсивністю 100 і 102 буде інтерпретуватися як один і той же колір.

`target`

Об'єкт ImagickPixel або рядок, який містить цільовий колір для малювання.

`x`

Початкова позиція заливки X.

`y`

Початкова позиція заливання Y.

`invert`

Якщо значення дорівнює **`true`**, зафарбовує будь-який піксель, що не відповідає цільовому кольору.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::floodfillPaintImage()****

```php
<?php

/* Создание нового объекта Imagick */
$im = new Imagick();

/* Создание красных, зеленых и синих изображения */
$im->newImage(100, 50, "red");
$im->newImage(100, 50, "green");
$im->newImage(100, 50, "blue");

/* Сложение изображений в одно*/
$im->resetIterator();
$combined = $im->appendImages(true);

/* Сохранение промежуточного изображения для сравнения */
$combined->writeImage("floodfillpaint_intermediate.png");

/* Целевой пиксель для рисования */
$x = 1;
$y = 1;

/* Получение цвета, которым рисуем */
$target = $combined->getImagePixelColor($x, $y);

/* Закрашивание пикселя в позиции 1,1 черным и всех соседних пикселей,
   соответствующих целевому цвету */
$combined->floodfillPaintImage("black", 1, $target, $x, $y, false);

/* Сохранение результата */
$combined->writeImage("floodfillpaint_result.png");
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Imagick::floodfillPaintImage()](images/c0d23d2d6769e53e24a1b3136c064577-floodfillpaint_intermediate.png)

![Висновок прикладу: Imagick::floodfillPaintImage()](images/c0d23d2d6769e53e24a1b3136c064577-floodfillpaint_result.png)
