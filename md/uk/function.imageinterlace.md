---
navigation:
  - function.imagegrabwindow.md: « imagegrabwindow
  - function.imageistruecolor.md: imageistruecolor »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageinterlace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Если значение\*\*`true`**, изображение будет разбито на чередующиеся строки, в противном случае бит интерлейсинга будет установлен в**`false`\*\*

### Значення, що повертаються

Повертає **`true`**, если бит интерлейсинга установлен,**`false`** в іншому випадку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.5 | **imageinterlace()** тепер повертає логічне значення (bool); раніше вона повертала ціле число (int). (Ненульове значення для зображень з інтерлейсингом, інакше - нуль). |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | `enable` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |

### Приклади

**Пример #1 Включение интерлейсинга, используя**imageinterlace()\*\*\*\*

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
