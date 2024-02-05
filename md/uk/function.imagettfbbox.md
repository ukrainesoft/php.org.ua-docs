---
navigation:
  - function.imagetruecolortopalette.md: « imagetruecolortopalette
  - function.imagettftext.md: imagettftext »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagettfbbox
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagettfbbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imagettfbbox — Отримання параметрів рамки, що обрамляє текст написаний TrueType шрифтом

### Опис

```methodsynopsis
imagettfbbox(    float $size,    float $angle,    string $font_filename,    string $string,    array $options = []): array|false
```

Ця функція розраховує та повертає параметри рамки навколо тексту TrueType у пікселах.

> **Зауваження** :
> 
> До PHP 8.0.0[imageftbbox()](function.imageftbbox.md) - це розширений варіант **imagettfbbox()** який додатково підтримує `extrainfo`. Починаючи з PHP 8.0.0, \*\*imagettfbbox()\*\*является псевдонимом[imageftbbox()](function.imageftbbox.md)

### Список параметрів

`size`

Розмір шрифту у типографських пунктах.

`angle`

Кут у градусах у якому буде виміряний `string`

`fontfile`

Шлях до шрифту TrueType, який потрібно використовувати.

Залежно від того, яка бібліотека GD завантажена в PHP, *якщо параметр `fontfile` не починається із символу , то к имени файла будет добавлено расширение`.ttf`* і бібліотека намагатиметься шукати це ім'я файлу за певною бібліотекою шляху шрифтів.

При роботі з бібліотекою GD версії нижче 2.0.18 як роздільник шляхів для різних файлів шрифтів буде використано символ `пробілу`, а не крапка з комою. Ненавмисне використання цієї особливості призведе до попередження: `Warning: Could not find/open font`. Єдиним коректним рішенням для цих версій бібліотек буде переміщення файлів шрифтів до директорії, що не містить пробілів.

У багатьох випадках, коли шрифт знаходиться в тому ж каталозі, що і PHP скрипт, допоможе наступний трюк.

```php
<?php
// Установка переменной окружения для GD
putenv('GDFONTPATH=' . realpath('.'));

// Имя шрифта для использования (обратите внимание, что расширение .ttf не указывается)
$font = 'SomeFont';
?>
```

> **Зауваження** :
> 
> Обратите внимание, что[open\_basedir](ini.core.md#ini.open-basedir) *не*применяется к`fontfile`

`string`

Вимірюваний рядок.

### Значення, що повертаються

**imagettfbbox()** повертає масив з 8 елементів, що представляють координати чотирьох точок - вершин рамки навколо тексту. У разі помилки функція поверне **`false`**

| ключ | содержимое |
| --- | --- |
|  | нижній лівий кут, X координата |
|  | нижній лівий кут, Y координата |
|  | нижній правий кут, X координата |
| 3 | нижній правий кут, Y координата |
| 4 | верхній правий кут, X координата |
| 5 | верхній правий кут, Y координата |
| 6 | верхній лівий кут, X координата |
| 7 | верхній лівий кут, Y координата |

Крапки розраховані щодо тексту *text*и независимо от угла`angle`. . Тобто верхній лівий означає верхній лівий кут, якщо дивитися на текст горизонтально.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Добавлен параметр`options` |

### Приклади

**Приклад #1 Приклад використання** imagettfbbox()\*\*\*\*

```php
<?php
// создание изображения 300x150
$im = imagecreatetruecolor(300, 150);
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);

// Белый фон
imagefilledrectangle($im, 0, 0, 299, 299, $white);

// Путь к файлу шрифта
$font = './arial.ttf';

// создаём рамку для текста
$bbox = imagettfbbox(10, 45, $font, 'Powered by PHP ' . phpversion());

// наши координаты X и Y
$x = $bbox[0] + (imagesx($im) / 2) - ($bbox[4] / 2) - 25;
$y = $bbox[1] + (imagesy($im) / 2) - ($bbox[5] / 2) - 5;

// Пишем текст
imagettftext($im, 10, 45, $x, $y, $black, $font, 'Powered by PHP ' . phpversion());

// создаём другую рамку для другого текста
$bbox = imagettfbbox(10, 45, $font, 'and Zend Engine ' . zend_version());

// задаём координаты так, чтобы текст шёл сразу за первой надписью
$x = $bbox[0] + (imagesx($im) / 2) - ($bbox[4] / 2) + 10;
$y = $bbox[1] + (imagesy($im) / 2) - ($bbox[5] / 2) - 5;

// Пишем вторую надпись
imagettftext($im, 10, 45, $x, $y, $black, $font, 'and Zend Engine ' . zend_version());

// Вывод в броузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Примітки

> **Зауваження**: Ця функція доступна лише у випадку, якщо PHP був скомпільований з підтримкою freetype (**\--with-freetype-dir=DIR**) .

### Дивіться також

-   [imagettftext()](function.imagettftext.md) \- Малювання тексту на зображенні шрифтом TrueType
-   [imageftbbox()](function.imageftbbox.md) \- Визначення меж тексту, що виводиться шрифтом freetype2
