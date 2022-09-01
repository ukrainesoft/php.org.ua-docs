---
navigation:
  - function.imagefontwidth.html: « imagefontwidth
  - function.imagefttext.html: imagefttext »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imageftbbox
---
# imageftbbox

(PHP 4> = 4.0.7, PHP 5, PHP 7, PHP 8)

imageftbbox — Визначення меж тексту, що виводиться шрифтом freetype2

### Опис

```methodsynopsis
imageftbbox(    float $size,    float $angle,    string $font_filename,    string $string,    array $options = []): array|false
```

Ця функція розраховує та повертає рамку (кордон) FreeType тексту.

> **Зауваження**
> 
> До PHP 8.0.0 **imageftbbox()** - це розширений варіант [imagettfbbox()](function.imagettfbbox.html), який додатково підтримує `extrainfo`. Починаючи з 8.0.0, [imagettfbbox()](function.imagettfbbox.html) є псевдонімом **imageftbbox()**

### Список параметрів

`size`

Розмір шрифту у типографських пунктах.

`angle`

Кут у градусах у якому `string` має бути виміряний.

`font_filename`

Ім'я файлу шрифту TrueType (може бути URL). Залежно від версії GD бібліотеки функція може спробувати знайти файли, які не починаються з '/' шляхом додавання '.ttf' в кінець імені файлу та пошуку за адресою, заданою в бібліотеці.

`string`

Вимірюваний рядок.

`options`

**Можливі ключі масиву `options`**

| Ключ | Тип | Значение |
| --- | --- | --- |
| `linespacing` | float | Визначає малювання підкреслювань |

### Значення, що повертаються

**imageftbbox()** повертає масив з 8 елементів, що представляють чотири точки в кутах рамки тексту, що обрамляє:

<table class="doctable informaltable"><tbody class="tbody"><tr><td>0</td><td>нижній лівий кут, X координата</td></tr><tr><td>1</td><td>нижній лівий кут, координата Y</td></tr><tr><td>2</td><td>нижній правий кут, X координата</td></tr><tr><td>3</td><td>нижній правий кут, координата Y</td></tr><tr><td>4</td><td>верхній правий кут, X координата&lt; /td&gt;</td></tr><tr><td>5</td><td>верхній правий кут, координата Y</td></tr><tr><td>6</td><td>верхній лівий кут, координата X</td></tr><tr><td>7</td><td>верхній лівий кут, Y координата</td></tr></tbody></table>

Крапки розташовані щодо тексту *text* і не залежать від кута `angle`, таким чином "верхній лівий" означає верхню ліву точку тексту, якщо розташувати текст горизонтально.

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **imageftbbox()****

```php
<?php
// Создание изображения 300x150
$im = imagecreatetruecolor(300, 150);
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);

// установка белого фона
imagefilledrectangle($im, 0, 0, 299, 299, $white);

// путь к файлу шрифта
$font = './arial.ttf';

// создаём рамку вокруг текста
$bbox = imageftbbox(10, 0, $font, 'Группа документирования PHP');

// наши координаты для X и Y
$x = $bbox[0] + (imagesx($im) / 2) - ($bbox[4] / 2) - 5;
$y = $bbox[1] + (imagesy($im) / 2) - ($bbox[5] / 2) - 5;

imagefttext($im, 10, 0, $x, $y, $black, $font, 'Группа документирования PHP');

// вывод в броузер
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### Примітки

> **Зауваження**: Ця функція доступна лише у випадку, якщо PHP був скомпільований за допомогою freetype (**\-with-freetype-dir=DIR**

### Дивіться також

-   [imagefttext()](function.imagefttext.html) - Нанесення тексту на зображення за допомогою шрифтів FreeType 2
-   [imagettfbbox()](function.imagettfbbox.html) - Отримання параметрів рамки, що обрамляє текст написаний TrueType шрифтом
