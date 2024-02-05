---
navigation:
  - function.imageresolution.md: « imageresolution
  - function.imagesavealpha.md: imagesavealpha »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagerotate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagerotate

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

imagerotate — Повертання зображення із заданим кутом.

### Опис

```methodsynopsis
imagerotate(GdImage $image, float $angle, int $background_color): GdImage|false
```

Поворот изображения`image` на заданий кут `angle` у градусах.

Центром повороту є центр зображення. Повертається зображення може відрізнятися розміром від оригіналу.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`angle`

Кут повороту в градусах проти годинникової стрілки.

`background_color`

Колір фон вільної зони після повороту.

### Значення, що повертаються

Повертає об'єкт поверненого зображення у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Параметр, що не використовується`ignore_transparent` був повністю вилучений. |
| 8.0.0 | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | Невикористовуваний `v` тепер очікує на логічне значення (bool); раніше очікувалося ціле число (int). |

### Приклади

**Приклад #1 Повертання зображення на 180 градусів**

Цей приклад повертає зображення на 180 градусів – верхи вниз.

```php
<?php
// Файл и угол поворота
$filename = 'test.jpg';
$degrees = 180;

// Тип содержимого
header('Content-type: image/jpeg');

// Загрузка изображения
$source = imagecreatefromjpeg($filename);

// Поворот
$rotate = imagerotate($source, $degrees, 0);

// Вывод
imagejpeg($rotate);

// Высвобождение памяти
imagedestroy($source);
imagedestroy($rotate);
?>
```

Висновок наведеного прикладу буде схожим на:

![Приклад виведе зображення, повернене на 180 градусів.](images/21009b70229598c6a80eef8b45bf282b-imagerotate.jpg)

### Примітки

> **Зауваження** :
> 
> Ця функція піддається впливу методу інтерполяції, встановленим функцією [imagesetinterpolation()](function.imagesetinterpolation.md)

### Дивіться також

-   [imagesetinterpolation()](function.imagesetinterpolation.md) \- встановлює метод інтерполяції
