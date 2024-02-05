---
navigation:
  - imagick.haspreviousimage.md: '« Imagick::hasPreviousImage'
  - imagick.identifyimage.md: 'Imagick::identifyImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::identifyFormat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::identifyFormat

(PECL imagick 3 >= 3.3.0)

Imagick::identifyFormat — Замінює будь-які вбудовані символи форматування відповідною властивістю зображення

### Опис

```methodsynopsis
public Imagick::identifyFormat(string $embedText): string|false
```

Замінює будь-які вбудовані символи форматування відповідною властивістю зображення та повертає інтерпретований текст. Подивіться [http://www.imagemagick.org/script/escape.php](http://www.imagemagick.org/script/escape.php), щоб дізнатися про послідовність екранування.

### Список параметрів

`embedText`

Рядок, що містить послідовності форматування, наприклад, "Поле обрізки: %@ кількість унікальних кольорів: %k".

### Значення, що повертаються

Повертає формат або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Imagick::identifyFormat()\*\*\*\*

```php
<?php
        $output = "Вывод 'Поле обрезки: %@ количество уникальных цветов: %k': <br/>";
        $imagick = new \Imagick(realpath("./images/artifact/mask.png"));
        $output .= $imagick->identifyFormat("Поле обрезки: %@ количество уникальных цветов: %k");

?>
```
