---
navigation:
  - imagick.haspreviousimage.html: '« Imagick::hasPreviousImage'
  - imagick.identifyimage.html: 'Imagick::identifyImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::identifyFormat'
---
# Imagick::identifyFormat

(PECL imagick 3> = 3.3.0)

Imagick::identifyFormat — Опис

### Опис

```methodsynopsis
public Imagick::identifyFormat(string $embedText): string|false
```

Замінює будь-які вбудовані символи форматування відповідною властивістю зображення та повертає інтерпретований текст. Подивіться [http://www.imagemagick.org/script/escape.php](http://www.imagemagick.org/script/escape.php), щоб дізнатися про послідовність екранування.

### Список параметрів

`embedText`

Рядок, що містить послідовності форматування, наприклад, "Поле обрізки: %@ кількість унікальних кольорів: %k".

### Значення, що повертаються

Повертає формат або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::identifyFormat()****

```php
<?php
        $output = "Вывод 'Поле обрезки: %@ количество уникальных цветов: %k': <br/>";
        $imagick = new \Imagick(realpath("./images/artifact/mask.png"));
        $output .= $imagick->identifyFormat("Поле обрезки: %@ количество уникальных цветов: %k");

?>
```
