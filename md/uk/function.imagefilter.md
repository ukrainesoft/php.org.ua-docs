Застосовує фільтр до зображення

-   [« imagefilltoborder](function.imagefilltoborder.md)
    
-   [imageflip »](function.imageflip.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Застосовує фільтр до зображення
    

# imagefilter

(PHP 5, PHP 7, PHP 8)

imagefilter — Застосовує фільтр до зображення

### Опис

```methodsynopsis
imagefilter(GdImage $image, int $filter, array|int|float|bool ...$args): bool
```

**imagefilter()** застосовує заданий фільтр `filter` до зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`filter`

`filter` може бути одним з наступних:

-   **`IMG_FILTER_NEGATE`**: Інвертує всі кольори зображення
-   **`IMG_FILTER_GRAYSCALE`**: Перетворює кольори зображення в градації сірого шляхом перетворення компонентів червоного, зеленого та синього на їхню суму з урахуванням ваг, таких як при обчисленні яскравості (Y') по REC.601. Альфа-канал зберігається. Для зображень, що використовують палітру, результат може відрізнятися через обмеження, що накладаються палітрою.
-   **`IMG_FILTER_BRIGHTNESS`**: Змінює яскравість зображення. Використовуйте аргумент `args` для завдання рівня яскравості. Діапазон яскравостей від -255 до 255.
-   **`IMG_FILTER_CONTRAST`**: Змінює контрастність зображення. Використовуйте аргумент `args` для завдання рівня контрастності.
-   **`IMG_FILTER_COLORIZE`**: Те саме, що і **`IMG_FILTER_GRAYSCALE`**, за винятком того, що можна встановити колір. Використовуйте аргументи `args` `arg2` і `arg3` для вказівки каналів `red` `green` `blue`, а `arg4` для `alpha` каналу. Діапазон кожного каналу кольору від 0 до 255.
-   **`IMG_FILTER_EDGEDETECT`**: Використовує визначення меж для їх підсвічування
-   **`IMG_FILTER_EMBOSS`**: Додає рельєф
-   **`IMG_FILTER_GAUSSIAN_BLUR`**: Розмиває зображення за методом Гауса.
-   **`IMG_FILTER_SELECTIVE_BLUR`**: Розмиває зображення.
-   **`IMG_FILTER_MEAN_REMOVAL`**: Використовує усереднення для досягнення ефекту "ескізу"
-   **`IMG_FILTER_SMOOTH`**: Робить межі більш плавними, а зображення менш чітким. Використовуйте аргумент `args` для завдання рівня гладкості.
-   **`IMG_FILTER_PIXELATE`**: Застосовує ефект пікселювання. Використовуйте аргумент `args` для завдання розміру блоку та аргумент `arg2` для завдання режиму пікселювання.
-   **`IMG_FILTER_SCATTER`**: Застосовує ефект розсіювання зображення, використовуйте `args` і `arg2` для визначення сили ефекту та додатково `arg3` для використання лише до вибраних кольорів пікселів.

`args`

-   **`IMG_FILTER_BRIGHTNESS`**: Рівень яскравості
-   **`IMG_FILTER_CONTRAST`**: Рівень контрастності
-   **`IMG_FILTER_COLORIZE`**: Значення червоного кольору.
-   **`IMG_FILTER_SMOOTH`**: Рівень згладжування.
-   **`IMG_FILTER_PIXELATE`**: Розмір блоку у пікселах.
-   **`IMG_FILTER_SCATTER`**: Рівень зменшення ефекту Не повинен бути більшим або дорівнює рівню додавання ефекту, встановленому за допомогою `arg2`

`arg2`

-   **`IMG_FILTER_COLORIZE`**: Значення зеленого кольору.
-   **`IMG_FILTER_PIXELATE`**: Використовувати вдосконалений ефект пікселювання чи ні (за замовчуванням **`false`**
-   **`IMG_FILTER_SCATTER`**: Рівень додавання ефекту.

`arg3`

-   **`IMG_FILTER_COLORIZE`**: Значення синього кольору.
-   **`IMG_FILTER_SCATTER`**: Необов'язковий масив значень індексації кольору для ефекту.

`arg4`

-   **`IMG_FILTER_COLORIZE`**: Альфа канал, значення між 0 та 127. 0 означає непрозорість, 127 відповідає абсолютній прозорості.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |
|  | Додано підтримку розсіювання (**`IMG_FILTER_SCATTER`** |

### Приклади

**Приклад #1 Приклад використання **imagefilter()** із фільтром grayscale**

```php
<?php
$im = imagecreatefrompng('dave.png');

if($im && imagefilter($im, IMG_FILTER_GRAYSCALE))
{
    echo 'Изображение преобразовано к градациям серого.';

    imagepng($im, 'dave.png');
}
else
{
    echo 'Преобразование не удалось.';
}

imagedestroy($im);
?>
```

**Приклад #2 Приклад використання **imagefilter()** з фільтром яскравості**

```php
<?php
$im = imagecreatefrompng('sean.png');

if($im && imagefilter($im, IMG_FILTER_BRIGHTNESS, 20))
{
    echo 'Яркость изображения изменена.';

    imagepng($im, 'sean.png');
    imagedestroy($im);
}
else
{
    echo 'Изменить яркость не удалось.';
}
?>
```

**Приклад #3 Приклад використання **imagefilter()** з фільтром colorize**

```php
<?php
$im = imagecreatefrompng('philip.png');

/* R, G, B, so 0, 255, 0 is green */
if($im && imagefilter($im, IMG_FILTER_COLORIZE, 0, 255, 0))
{
    echo 'Изображение преобразовано к оттенкам зеленого.';

    imagepng($im, 'philip.png');
    imagedestroy($im);
}
else
{
    echo 'Преобразование не удалось.';
}
?>
```

**Приклад #4 Приклад використання **imagefilter()** з фільтром negate**

```php
<?php
// Определим нашу функцию, которую можно использовать в PHP
// без imagefilter()
function negate($im)
{
    if(function_exists('imagefilter'))
    {
        return imagefilter($im, IMG_FILTER_NEGATE);
    }

    for($x = 0; $x < imagesx($im); ++$x)
    {
        for($y = 0; $y < imagesy($im); ++$y)
        {
            $index = imagecolorat($im, $x, $y);
            $rgb = imagecolorsforindex($index);
            $color = imagecolorallocate($im, 255 - $rgb['red'], 255 - $rgb['green'], 255 - $rgb['blue']);

            imagesetpixel($im, $x, $y, $color);
        }
    }

    return(true);
}

$im = imagecreatefromjpeg('kalle.jpg');

if($im && negate($im))
{
    echo 'Изображение инвертировано успешно.';

    imagejpeg($im, 'kalle.jpg', 100);
    imagedestroy($im);
}
else
{
    echo 'Инвертировать изображение не удалось.';
}
?>
```

**Приклад #5 Приклад використання **imagefilter()** з фільтром pixelate**

```php
<?php
// загрузка PHP логотипа, нам нужно 2 штуки
// для сравнения
$logo1 = imagecreatefrompng('./php.png');
$logo2 = imagecreatefrompng('./php.png');

// подопытный экземпляр
$output = imagecreatetruecolor(imagesx($logo1) * 2, imagesy($logo1));

// Применение пикселирования к каждому изображению с размером блока в 3 пиксела
imagefilter($logo1, IMG_FILTER_PIXELATE, 3);
imagefilter($logo2, IMG_FILTER_PIXELATE, 3, true);

// Совмещение различий в выходном изображении
imagecopy($output, $logo1, 0, 0, 0, 0, imagesx($logo1) - 1, imagesy($logo1) - 1);
imagecopy($output, $logo2, imagesx($logo2), 0, 0, 0, imagesx($logo2) - 1, imagesy($logo2) - 1);
imagedestroy($logo1);
imagedestroy($logo2);

// Вывод различий
header('Content-Type: image/png');
imagepng($output);
imagedestroy($output);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefilter() pixelate](images/21009b70229598c6a80eef8b45bf282b-imagefilterpixelate.png)

**Приклад #6 Приклад використання **imagefilter()** з фільтром scatter**

```php
<?php
// Загрузка изображения
$logo = imagecreatefrompng('./php.png');

// Применение очень мягкого эффекта рассеивания к изображению
imagefilter($logo, IMG_FILTER_SCATTER, 3, 5);

// Вывов изображения с эффектом рассеивания
header('Content-Type: image/png');
imagepng($logo);
imagedestroy($logo);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefilter() scatter](images/21009b70229598c6a80eef8b45bf282b-scatter.png)

### Примітки

> **Зауваження**: Результат **`IMG_FILTER_SCATTER`** завжди випадковий.

### Дивіться також

-   [imageconvolution()](function.imageconvolution.md) - Накладання викривляючої матриці 3х3, використовуючи коефіцієнт та зміщення