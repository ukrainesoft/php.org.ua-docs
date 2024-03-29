---
navigation:
  - function.imageftbbox.md: « imageftbbox
  - function.imagegammacorrect.md: imagegammacorrect »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefttext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagefttext

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

imagefttext — Нанесення тексту на зображення за допомогою шрифтів FreeType 2

### Опис

```methodsynopsis
imagefttext(    GdImage $image,    float $size,    float $angle,    int $x,    int $y,    int $color,    string $font_filename,    string $text,    array $options = []): array|false
```

> **Зауваження** :
> 
> До PHP 8.0.0**imagefttext()** - це розширений варіант [imagettftext()](function.imagettftext.md), який додатково підтримує `extrainfo`. Починаючи з PHP 8.0.0, [imagettftext()](function.imagettftext.md)является псевдонимом**imagefttext()**

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`size`

Розмір шрифту у пунктах.

`angle`

Кут у градусах, 0 градусів означає розташування тексту зліва направо. Позитивні значення означає поворот тексту проти годинникової стрілки. Наприклад, текст, повернутий на 90 градусів, потрібно буде читати знизу вгору.

`x`

Координати `x`и`y` визначають відправну точку першого символу тексту (конкретно, лівий нижній кут символу). Тут є відмінність від функції [imagestring()](function.imagestring.md), в якій `x`и`y` визначають лівий верхній кут першого символу. Наприклад, верхній лівий має координати 0,0.

`y`

y-координат. Це позиція базової лінії шрифту, у випадку вона не збігається з нижчою точкою в символі.

`color`

Индекс требуемого цвета текста, смотрите[imagecolorexact()](function.imagecolorexact.md)

`font_filename`

Шлях до TrueType шрифту, який потрібно використовувати.

Залежно від версії GD бібліотеки *якщо `font_filename` не починається з , то в конец названия файла будет добавлено расширение`.ttf`*, та бібліотека намагатиметься знайти цей файл за адресою, визначеною в налаштуваннях бібліотеки.

Найчастіше розміщення файлів шрифтів у директорії скрипта вирішує подібні проблеми включення файлів.

```php
<?php
// Задание переменной окружения для GD
putenv('GDFONTPATH=' . realpath('.'));

// Имя шрифта для использования (обратите внимание на отсутствие расширения .ttf)
$font = 'SomeFont';
?>
```

`text`

Текст для вставлення зображення.

`options`

**Можливі значення масиву `options`**

| Ключ | Тип | Значение |
| --- | --- | --- |
| `linespacing` | float | Визначає малювання нижнього підкреслення |

### Значення, що повертаються

Ця функція повертає масив, який визначає чотири точки рамки тексту. Текст усередині цих кордонів починається з лівого нижнього кута і повертається проти годинникової стрілки:

<table class="doctable informaltable"><tbody class="tbody"><tr><td>0</td><td>нижняя левая x-координата</td></tr><tr><td>1</td><td>нижняя левая y-координата</td></tr><tr><td>2</td><td>нижняя правая x-координата</td></tr><tr><td>3</td><td>нижняя правая y-координата</td></tr><tr><td>4</td><td>верхняя правая x-координата</td></tr><tr><td>5</td><td>верхняя правая y-координата</td></tr><tr><td>6</td><td>верхняя левая x-координата</td></tr><tr><td>7</td><td>верхняя левая y-координата</td></tr></tbody></table>

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagefttext()\*\*\*\*

```php
<?php
// Создание изображения 300x100
$im = imagecreatetruecolor(300, 100);
$red = imagecolorallocate($im, 0xFF, 0x00, 0x00);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);

// Сделаем красный фон
imagefilledrectangle($im, 0, 0, 299, 99, $red);

// Путь к ttf файлу шрифта
$font_file = './arial.ttf';

// Рисуем текст 'PHP Manual' шрифтом 13го размера
imagefttext($im, 13, 0, 105, 55, $black, $font_file, 'PHP Manual');

// Вывод изображения
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Примітки

> **Зауваження**: Ця функція доступна лише у випадку, якщо PHP був скомпільований з підтримкою freetype (**\--with-freetype-dir=DIR**) .

### Дивіться також

-   [imageftbbox()](function.imageftbbox.md) \- Визначення меж тексту, що виводиться шрифтом freetype2
-   [imagettftext()](function.imagettftext.md) \- Малювання тексту на зображенні шрифтом TrueType
