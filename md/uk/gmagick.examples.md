---
navigation:
  - gmagick.constants.md: « Обумовлені константи
  - class.gmagick.md: Gmagick »
  - index.md: PHP Manual
  - book.gmagick.md: Gmagick
title: Приклади
---
# Приклади

Наступний код показує часто використовувані операції Gmagick над зображеннями.

**Приклад #1 Приклади використання Gmagick**

```php
<?php
// Создаём новый объект Gmagick
$image = new Gmagick('example.jpg');

// Создаём уменьшенную копию изображения. 0 для сохранения пропорций.
$image->thumbnailimage(100, 0);

// Создаём рамку вокруг изображения, после чего накладываем эффект масляной краски
// Обратите внимание на цепочки преобразующих методов, поддерживаемых в gmagick
$image->borderimage("yellow", 8, 8)->oilpaintimage(0.3);

// Записываем полученное изображение в файл
$image->write('example_thumbnail.jpg');
?>
```
