---
navigation:
  - function.imagefilter.md: « imagefilter
  - function.imagefontheight.md: imagefontheight »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imageflip
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imageflip

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

imgflip — Перетворення зображення за допомогою вибраного режиму.

### Опис

```methodsynopsis
imageflip(GdImage $image, int $mode): bool
```

Перевертає зображення `image`, використовуючи вибраний режим `mode`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`mode`

Режим переворота - одна из констант\*\*`IMG_FLIP_*`\*\* :

| Константа | Опис |
| --- | --- |
| **`IMG_FLIP_HORIZONTAL`** | Перевертає зображення по горизонталі. |
| **`IMG_FLIP_VERTICAL`** | Перевертає зображення по вертикалі. |
| **`IMG_FLIP_BOTH`** | Перевертає зображення по горизонталі і по вертикалі. |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Перевертає зображення по вертикалі**

У цьому прикладі використовується константа **`IMG_FLIP_VERTICAL`**

```php
<?php
// Файл
$filename = 'phplogo.png';

// Тип данных
header('Content-type: image/png');

// Загрузка
$im = imagecreatefrompng($filename);

// Переворачиваем по вертикали
imageflip($im, IMG_FLIP_VERTICAL);

// Вывод
imagejpeg($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Результат прикладу: Перевернуте по вертикалі зображення](images/21009b70229598c6a80eef8b45bf282b-imageflipvertical.png)

**Приклад #2 Перевертає зображення по горизонталі**

У цьому прикладі використовується константа **`IMG_FLIP_HORIZONTAL`**

```php
<?php
// Файл
$filename = 'phplogo.png';

// Тип данных
header('Content-type: image/png');

// Загрузка
$im = imagecreatefrompng($filename);

// Переворачиваем по горизонтали
imageflip($im, IMG_FLIP_HORIZONTAL);

// Вывод
imagejpeg($im);
imagedestroy($im);
?>
```

Висновок наведеного прикладу буде схожим на:

![Результат прикладу: Перевернуте по горизонталі зображення](images/21009b70229598c6a80eef8b45bf282b-imagefliphorizontal.png)
