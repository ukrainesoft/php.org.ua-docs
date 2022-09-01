---
navigation:
  - function.imagedashedline.html: « imagedashedline
  - function.imageellipse.html: imageellipse »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagedestroy
---
# imagedestroy

(PHP 4, PHP 5, PHP 7, PHP 8)

imagedestroy — Знищення зображення

### Опис

```methodsynopsis
imagedestroy(GdImage $image): bool
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

До PHP 8.0.0, **imagedestroy()** звільняє пам'ять, зайняту зображенням `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер є NOP. |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagedestroy()** до PHP 8.0.0**

```php
<?php
// Создание изображения 100 x 100
$im = imagecreatetruecolor(100, 100);

// изменение или сохранение изображения

// освобождение памяти
imagedestroy($im);
?>
```
