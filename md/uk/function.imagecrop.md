---
navigation:
  - function.imagecreatetruecolor.md: « imagecreatetruecolor
  - function.imagecropauto.md: imagecropauto »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecrop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecrop

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

imagecrop — Обрізати зображення до прямокутника.

### Опис

```methodsynopsis
imagecrop(GdImage $image, array $rectangle): GdImage|false
```

Обрізає зображення до заданої прямокутної області та повертає отримане зображення. Заданий параметр `image`не изменяется.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`rectangle`

Обрізаний прямокутник у вигляді масиву (array) із ключами `x` `y` `width`и`height`

### Значення, що повертаються

Повертає об'єкт обрізаного зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagecrop()\*\*\*\*

У цьому прикладі показано, як обрізати зображення до квадратної області.

```php
<?php
$im = imagecreatefrompng('example.png');
$size = min(imagesx($im), imagesy($im));
$im2 = imagecrop($im, ['x' => 0, 'y' => 0, 'width' => $size, 'height' => $size]);
if ($im2 !== FALSE) {
    imagepng($im2, 'example-cropped.png');
    imagedestroy($im2);
}
imagedestroy($im);
?>
```

### Дивіться також

-   [imagecropauto()](function.imagecropauto.md) \- Обрізає зображення автоматично на основі заданого режиму
