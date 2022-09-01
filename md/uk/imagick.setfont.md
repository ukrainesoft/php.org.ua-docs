---
navigation:
  - imagick.setfirstiterator.html: '« Imagick::setFirstIterator'
  - imagick.setformat.html: 'Imagick::setFormat »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setFont'
---
# Imagick::setFont

(PECL imagick 2> = 2.1.0, PECL imagick 3)

Imagick::setFont — Встановлює шрифт

### Опис

```methodsynopsis
public Imagick::setFont(string $font): bool
```

Встановлює об'єкт властивість шрифт. Метод можна використовувати, наприклад, для встановлення шрифту для caption: формат псевдозображень. Шрифт має бути налаштований у конфігурації ImageMagick або має існувати файл з ім'ям `font`. Метод не слід плутати з методом [ImagickDraw::setFont()](imagickdraw.setfont.md), який встановлює шрифт певного об'єкта ImagickDraw. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.7 або старшим.

### Список параметрів

`font`

Ім'я шрифту чи файлу.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setFont()****

Приклад використання Imagick::setFont

```php
<?php
/* Создание нового объекта Imagick */
$im = new Imagick();

/* Установка шрифта для объекта */
$im->setFont("example.ttf");

/* Создание нового заголовка */
$im->newPseudoImage(100, 100, "caption:Hello");

/* Работа с изображением */
?>
```

### Дивіться також

-   [Imagick::getFont()](imagick.getfont.md) - Повертає назву шрифту
-   [ImagickDraw::setFont()](imagickdraw.setfont.md) - Встановлює вказаний шрифт для використання під час анотування текстом
-   [ImagickDraw::getFont()](imagickdraw.getfont.md) - Повертає шрифт
