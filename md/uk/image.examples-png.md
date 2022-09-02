---
navigation:
  - image.examples.md: « Приклади
  - image.examples-watermark.md: Додавання водяних знаків на зображення за допомогою альфа-каналів »
  - index.md: PHP Manual
  - image.examples.md: Приклади
title: Створення PNG засобами PHP
---
## Створення PNG засобами PHP

**Приклад #1 Створення PNG засобами PHP**

```php
<?php

header("Content-type: image/png");
$string = $_GET['text'];
$im     = imagecreatefrompng("images/button1.png");
$orange = imagecolorallocate($im, 220, 210, 60);
$px     = (imagesx($im) - 7.5 * strlen($string)) / 2;
imagestring($im, 3, $px, 9, $string, $orange);
imagepng($im);
imagedestroy($im);

?>
```

Цей приклад можна було б викликати на сторінці з тегом: `<img src="button.php?text=text">`. Наведений вище скрипт button.php візьме рядок `"text"` та накладе її поверх базового зображення, яке є, в даному випадку `"images/button1.png"` та виведе кінцеве зображення. Це дуже зручний спосіб, щоб уникнути необхідності створення нової кнопки щоразу, коли ви хочете змінити текст кнопки. За допомогою цього методу вона генерується динамічно.
