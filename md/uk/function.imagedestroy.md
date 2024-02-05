---
navigation:
  - function.imagedashedline.md: « imagedashedline
  - function.imageellipse.md: imageellipse »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagedestroy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagedestroy

(PHP 4, PHP 5, PHP 7, PHP 8)

imagedestroy — Знищення зображення

### Опис

```methodsynopsis
imagedestroy(GdImage $image): bool
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

До PHP 8.0.0,\*\*imagedestroy()\*\*освобождает память, занятую изображением`image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер є NOP. |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagedestroy()**до PHP 8.0.0**

```php
<?php
// Создание изображения 100 x 100
$im = imagecreatetruecolor(100, 100);

// изменение или сохранение изображения

// освобождение памяти
imagedestroy($im);
?>
```
