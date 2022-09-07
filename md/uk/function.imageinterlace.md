---
navigation:
  - function.imagegrabwindow.md: « imagegrabwindow
  - function.imageistruecolor.md: imageistruecolor »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageinterlace
---
# imageinterlace

(PHP 4, PHP 5, PHP 7, PHP 8)

imageinterlace — Увімкнення або вимкнення інтерлейсингу

### Опис

```methodsynopsis
imageinterlace(GdImage $image, ?bool $enable = null): bool
```

**imageinterlace()** перемикає стан біта інтерлейсингу.

Якщо встановити біт інтерлейсингу, а зображення завантажити як JPEG, це призведе до створення прогресивного JPEG.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`interlace`

Якщо значення **`true`**, зображення буде розбито на рядки, що чергуються, в іншому випадку біт інтерлейсингу буде встановлений в **`false`**

### Значення, що повертаються

Повертає **`true`**, якщо біт інтерлейсингу встановлено, **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | **imageinterlace()** тепер повертає логічне значення (bool); раніше вона повертала ціле число (int). (Ненульове значення для зображень з інтерлейсингом, інакше - нуль). |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |
|  | `enable` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |

### Приклади

**Приклад #1 Увімкнення інтерлейсингу за допомогою **imageinterlace()****

```php
<?php
// Создание нового изображения
$im = imagecreatefromgif('php.gif');

// Включение интерлейсинга
imageinterlace($im, true);

// Сохранение изображения
imagegif($im, './php_interlaced.gif');
imagedestroy($im);
?>
```
