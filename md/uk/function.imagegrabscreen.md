---
navigation:
  - function.imagegif.md: « imagegif
  - function.imagegrabwindow.md: imagegrabwindow »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegrabscreen
---
# imagegrabscreen

(PHP 5> = 5.2.2, PHP 7, PHP 8)

imagegrabscreen — Захоплює зображення з екрану

### Опис

```methodsynopsis
imagegrabscreen(): GdImage|false
```

Робить скріншот.

> **Зауваження**
> 
> Функція доступна лише у Windows.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання, **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagegrabscreen()****

У цьому прикладі показано, як зробити знімок екрана і зберегти його, як зображення png.

```php
<?php
$im = imagegrabscreen();
imagepng($im, "myscreenshot.png");
imagedestroy($im);
?>
```

### Дивіться також

-   [imagegrabwindow()](function.imagegrabwindow.md) - Захоплює зображення вікна
