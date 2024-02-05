---
navigation:
  - imagick.annotateimage.md: '« Imagick::annotateImage'
  - imagick.autolevelimage.md: 'Imagick::autoLevelImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::appendImages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::appendImages

(PECL imagick 2, PECL imagick 3)

Imagick::appendImages — Об'єднує набір зображень

### Опис

```methodsynopsis
public Imagick::appendImages(bool $stack): Imagick
```

Поєднує набір зображень в одне велике зображення.

### Список параметрів

`stack`

Чи варто складати зображення вертикально. За замовчуванням (або якщо зазначено **`false`**) зображення складаються зліва направо. Якщо `stack`установлен в\*\*`true`\*\*то зображення складаються зверху вниз.

### Значення, що повертаються

У разі успішного виконання повертає екземпляр Imagick.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::appendImages()\*\*\*\*

```php
<?php

/* Создаём новый объект imagick */
$im = new Imagick();

/* создаём красное, зелёное и синее изображения */
$im->newImage(100, 50, "red");
$im->newImage(100, 50, "green");
$im->newImage(100, 50, "blue");

/* Соединяем все изображения в одно */
$im->resetIterator();
$combined = $im->appendImages(true);

/* Выводим изображение */
$combined->setImageFormat("png");
header("Content-Type: image/png");
echo $combined;
?>
```

Висновок наведеного прикладу буде схожим на:

![Приклад висновку: Imagick::appendImages()](images/c0d23d2d6769e53e24a1b3136c064577-floodfillpaint_intermediate.png)
