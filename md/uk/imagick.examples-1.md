---
navigation:
  - imagick.examples.md: « Приклади
  - class.imagick.md: Imagick »
  - index.md: PHP Manual
  - imagick.examples.md: Приклади
title: Базове використання
---
## Базове використання

У PHP дуже легко керувати об'єктом Imagick, використовуючи об'єктно-орієнтований інтерфейс. Ось невеликий приклад, як зробити мініатюру:

**Приклад #1 Створення мініатюри в Imagick**

```php
<?php

header('Content-type: image/jpeg');

$image = new Imagick('image.jpg');

// Если в качестве ширины или высоты передан 0,
// то сохраняется соотношение сторон
$image->thumbnailImage(100, 0);

echo $image;

?>
```

З використанням SPL та інших об'єктно-орієнтованих функцій, що підтримуються в Imagick, можна дуже легко змінити розміри всіх файлів у директорії (корисно для пакетної зміни великих зображень з цифрової камери для перегляду в Web). Тут ми використовуємо зміну розміру, використовуючи певні мета-дані:

**Приклад #2 Створення мініатюр для всіх JPG файлів у директорії**

```php
<?php

$images = new Imagick(glob('images/*.JPG'));

foreach($images as $image) {

    // Передаём 0 в thumbnailImage для сохранения соотношения сторон
    $image->thumbnailImage(1024,0);

}

$images->writeImages();

?>
```

Цей приклад створює відображення зображення. Відображення створюється дзеркальним відображенням та накладенням градієнта на ньому. Потім оригінальне зображення та його відображення накладаються на полотно.

**Приклад #3 Створення відображення**

```php
<?php
/* Чтение изображения */
$im = new Imagick("test.png");

/* Миниатюра изображения */
$im->thumbnailImage(200, null);

/* Создание рамки для изображения */
$im->borderImage(new ImagickPixel("white"), 5, 5);

/* Клонируем изображение и зеркально поворачиваем его */
$reflection = $im->clone();
$reflection->flipImage();

/* Создаём градиент. Это будет наложением для отражения */
$gradient = new Imagick();

/* Градиент должен быть достаточно большой для изображения и его рамки */
$gradient->newPseudoImage($reflection->getImageWidth() + 10, $reflection->getImageHeight() + 10, "gradient:transparent-black");

/* Наложение градиента на отражение */
$reflection->compositeImage($gradient, imagick::COMPOSITE_OVER, 0, 0);

/* Добавляем прозрачность. Требуется ImageMagick 6.2.9 или выше */
$reflection->setImageOpacity( 0.3 );

/* Создаём пустой холст */
$canvas = new Imagick();

/* Холст должен быть достаточно большой, чтобы вместить оба изображения */
$width = $im->getImageWidth() + 40;
$height = ($im->getImageHeight() * 2) + 30;
$canvas->newImage($width, $height, new ImagickPixel("black"));
$canvas->setImageFormat("png");

/* Наложение оригинального изображения и отражения на холст */
$canvas->compositeImage($im, imagick::COMPOSITE_OVER, 20, 10);
$canvas->compositeImage($reflection, imagick::COMPOSITE_OVER, 20, $im->getImageHeight() + 10);

/* Вывод изображения */
header("Content-Type: image/png");
echo $canvas;
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад висновку: Створення відображення зображення](images/c0d23d2d6769e53e24a1b3136c064577-hello_world_reflection.png)

Цей приклад ілюструє використання заливки під час малювання.

**Приклад #4 Заливка тексту градієнтом**

```php
<?php

/* Создание нового объекта imagick */
$im = new Imagick();

/* Создание нового изображения. Будет использоваться как шаблон заливки */
$im->newPseudoImage(50, 50, "gradient:red-black");

/* Создаём объект imagickdraw */
$draw = new ImagickDraw();

/* Запускаем новый шаблон с названием "gradient" */
$draw->pushPattern('gradient', 0, 0, 50, 50);

/* Смешиваем градиент с шаблоном */
$draw->composite(Imagick::COMPOSITE_OVER, 0, 0, 50, 50, $im);

/* Закрываем шаблон */
$draw->popPattern();

/* Используем шаблон с названием "gradient" для заливки */
$draw->setFillPatternURL('#gradient');

/* Устанавливаем размер шрифта в 52 */
$draw->setFontSize(52);

/* Добавляем свой текст */
$draw->annotation(20, 50, "Hello World!");

/* Создаём новый объект холста и белое изображение */
$canvas = new Imagick();
$canvas->newImage(350, 70, "white");

/* Рисуем ImagickDraw на холсте */
$canvas->drawImage($draw);

/* устанавливаем чёрную рамку шириной 1px вокруг изображения */
$canvas->borderImage('black', 1, 1);

/* Устанавливаем формат PNG */
$canvas->setImageFormat('png');

/* Вывод изображения */
header("Content-Type: image/png");
echo $canvas;
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад виведення: Заливка тексту градієнтом](images/c0d23d2d6769e53e24a1b3136c064577-hello_world.png)

Робота з анімованими GIF-зображеннями

**Приклад #5 Читання GIF зображення та зміна розміру всіх кадрів**

```php
<?php

/* Создание нового объекта imagick и чтение в GIF */
$im = new Imagick("example.gif");

/* Изменение размера всех фреймов */
foreach ($im as $frame) {
    /* фреймы 50x50 */
    $frame->thumbnailImage(50, 50);

    /* Устанавливаем виртуальный холст для коррекции размера */
    $frame->setImagePage(50, 50, 0, 0);
}

/* Обратите внимание, writeImages вместо writeImage */
$im->writeImages("example_small.gif", true);
?>
```

Робота з примітивом "еліпс" та користувальницькими шрифтами

**Приклад #6 Create a PHP logo**

```php
<?php
/* Установка ширины и высоты в пропорции логотипа PHP */
$width = 400;
$height = 210;

/* Создание объекта Imagick с поддержкой прозрачности */
$img = new Imagick();
$img->newImage($width, $height, new ImagickPixel('transparent'));

/* Новый объект ImagickDraw  для отрисовки эллипса */
$draw = new ImagickDraw();
/* Установка пурпурного цвета заливки для эллипса */
$draw->setFillColor('#777bb4');
/* Задание размеров эллипса */
$draw->ellipse($width / 2, $height / 2, $width / 2, $height / 2, 0, 360);
/* Отрисовка эллипса */
$img->drawImage($draw);

/* Сброс цвета заливки с пурпурного на чёрный для текста (заметьте, что мы используем объект ImagickDraw повторно) */
$draw->setFillColor('black');
/* Задание обводки границы белым цветом */
$draw->setStrokeColor('white');
/* Задание толщины обводки */
$draw->setStrokeWidth(2);
/* Задание кернинга (отрицательные значения означают, что буквы будут ближе друг к другу) */
$draw->setTextKerning(-8);
/* Задание шрифта и его размера, которые используются в логотипе PHP */
$draw->setFont('Handel Gothic.ttf');
$draw->setFontSize(150);
/* Центрирование текста вертикально и горизонтально */
$draw->setGravity(Imagick::GRAVITY_CENTER);

/* Добавление текста "php" со смещением по Y на -10 на холст (внутри эллипса) */
$img->annotateImage($draw, 0, -10, 0, 'php');
$img->setImageFormat('png');

/* Установка соответвующего заголовка для PNG и вывод изображения */
header('Content-Type: image/png');
echo $img;
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад виведення : Створюється логотип PHP за допомогою Imagick](images/c0d23d2d6769e53e24a1b3136c064577-php_logo.png)
