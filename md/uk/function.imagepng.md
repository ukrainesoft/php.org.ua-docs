---
navigation:
  - function.imagepalettetotruecolor.md: « imagepalettetotruecolor
  - function.imagepolygon.md: imagepolygon »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagepng
---
# imagepng

(PHP 4, PHP 5, PHP 7, PHP 8)

imagepng — Виведення PNG зображення до браузера або файлу

### Опис

```methodsynopsis
imagepng(    GdImage $image,    resource|string|null $file = null,    int $quality = -1,    int $filters = -1): bool
```

Виводить або зберігає PNG зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`file`

Шлях, або відкритий потоковий ресурс (який автоматично закривається після завершення функції) для збереження файлу. Якщо не встановлено або дорівнює **`null`**, зображення буде виведено у потік виведення у бінарному вигляді.

> **Зауваження**
> 
> Неприпустимо передавати \*\*`null`\*\*якщо не використовуються аргументи `quality` і `filters`

`quality`

Ступінь стиснення: від 0 (немає стиснення) до 9. За замовчуванням (`-1`) використовується значення за промовчанням стиснення zlib. Детальніше читайте в [» руководстве по zlib](http://www.zlib.net/manual.md)

`filters`

Дозволяє зменшити розмір файлу PNG. Це бітова маска, значенням якої може бути комбінація констант `PNG_FILTER_XXX`. Для увімкнення або вимкнення всіх фільтрів зручно скористатися константами **`PNG_NO_FILTER`** або **`PNG_ALL_FILTERS`** відповідно. Значення за замовчуванням (`-1`) відключає фільтрацію.

**Застереження**

Параметр `filters` ігнорується системною бібліотекою libgd.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**Застереження**

Однак, якщо libgd не може вивести зображення, ця функція поверне **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

```php
<?php
$im = imagecreatefrompng("test.png");

header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Дивіться також

-   [imagegif()](function.imagegif.md) - Виводить зображення у браузер або пише у файл
-   [imagewbmp()](function.imagewbmp.md) - Виводить зображення у браузер або пише у файл
-   [imagejpeg()](function.imagejpeg.md) - Виводить зображення у браузер або пише у файл
-   [imagetypes()](function.imagetypes.md) - Повертає список типів зображень, які підтримує PHP збірка
-   [imagesavealpha()](function.imagesavealpha.md) - Чи зберігати повну інформацію альфа-каналу при збереженні зображень PNG
