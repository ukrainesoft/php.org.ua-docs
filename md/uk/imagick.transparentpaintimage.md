---
navigation:
  - imagick.transformimagecolorspace.md: '« Imagick::transformImageColorspace'
  - imagick.transposeimage.md: 'Imagick::transposeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::transparentPaintImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::transparentPaintImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::transparentPaintImage — Малює пікселі прозорими

### Опис

```methodsynopsis
public Imagick::transparentPaintImage(    mixed $target,    float $alpha,    float $fuzz,    bool $invert): bool
```

Малює пікселі, що відповідають цільовому кольору, прозорим. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.8 або старшим.

### Список параметрів

`target`

Цільовий колір для малювання

`alpha`

Рівень прозорості: 1.0 повністю непрозорий, тоді як 0.0 повністю прозорий.

`fuzz`

міра округлення (fuzz). Для прикладу, встановіть значення fuzz 10 і червоний колір з інтенсивністю 100 і 102 буде інтерпретуватися як один і той же колір.

`invert`

Якщо **`true`**, зафарбовує будь-який піксель, який відповідає цільовому кольору.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::transparentPaintImage()\*\*\*\*

```php
<?php
function transparentPaintImage($color, $alpha, $fuzz) {
    $imagick = new \Imagick(realpath("images/BlueScreen.jpg"));

    //Должен быть в формате, который поддерживает прозрачность
    $imagick->setimageformat('png');

    $imagick->transparentPaintImage(
        $color, $alpha, $fuzz * \Imagick::getQuantum(), false
    );

    //Не требуется, но помогает убирать оставленные пиксели
    $imagick->despeckleimage();

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
