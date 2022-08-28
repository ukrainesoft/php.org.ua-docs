Перевертає зображення, використовуючи вибраний режим

-   [« imagefilter](function.imagefilter.html)
    
-   [imagefontheight »](function.imagefontheight.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Перевертає зображення, використовуючи вибраний режим
    

# imgflip

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imgflip — Перетворення зображення за допомогою вибраного режиму.

### Опис

```methodsynopsis
imageflip(GdImage $image, int $mode): bool
```

Перевертає зображення `image`, використовуючи вибраний режим `mode`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`mode`

Режим перевороту - одна з констант **`IMG_FLIP_*`**

| Константа | Описание |
| --- | --- |
| **`IMG_FLIP_HORIZONTAL`** | Перевертає зображення по горизонталі. |
| **`IMG_FLIP_VERTICAL`** | Перевертає зображення по вертикалі. |
| **`IMG_FLIP_BOTH`** | Перевертає зображення по горизонталі і по вертикалі. |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Перевертає зображення по вертикалі**

У цьому прикладі використовується константа **`IMG_FLIP_VERTICAL`**

```php
<?php
// Файл
$filename = 'phplogo.png';

// Тип данных
header('Content-type: image/png');

// Загрузка
$im = imagecreatefrompng($filename);

// Переворачиваем по вертикали
imageflip($im, IMG_FLIP_VERTICAL);

// Вывод
imagejpeg($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Результат прикладу: Перевернуте по вертикалі зображення](images/21009b70229598c6a80eef8b45bf282b-imageflipvertical.png)

**Приклад #2 Перевертає зображення по горизонталі**

У цьому прикладі використовується константа **`IMG_FLIP_HORIZONTAL`**

```php
<?php
// Файл
$filename = 'phplogo.png';

// Тип данных
header('Content-type: image/png');

// Загрузка
$im = imagecreatefrompng($filename);

// Переворачиваем по горизонтали
imageflip($im, IMG_FLIP_HORIZONTAL);

// Вывод
imagejpeg($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Результат прикладу: Перевернуте по горизонталі зображення](images/21009b70229598c6a80eef8b45bf282b-imagefliphorizontal.png)