---
navigation:
  - function.imagegif.md: « imagegif
  - function.imagegrabwindow.md: imagegrabwindow »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagegrabscreen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagegrabscreen

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

imagegrabscreen — Захоплює зображення з екрану

### Опис

```methodsynopsis
imagegrabscreen(): GdImage|false
```

Робить скріншот.

> **Зауваження** :
> 
> Функція доступна лише у Windows.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання, \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**imagegrabscreen()\*\*\*\*

У цьому прикладі показано, як зробити знімок екрану і зберегти його, як зображення png.

```php
<?php
$im = imagegrabscreen();
imagepng($im, "myscreenshot.png");
imagedestroy($im);
?>
```

### Дивіться також

-   [imagegrabwindow()](function.imagegrabwindow.md) \- Захоплює зображення вікна
