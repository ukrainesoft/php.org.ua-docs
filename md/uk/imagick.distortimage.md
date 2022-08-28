Спотворює зображення, використовуючи різні методи спотворення

-   [« Imagick::displayImages](imagick.displayimages.html)
    
-   [Imagick::drawImage »](imagick.drawimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Спотворює зображення, використовуючи різні методи спотворення
    

# Imagick::distortImage

(PECL imagick 2> = 2.0.1, PECL imagick 3)

Imagick::distortImage — Спотворює зображення, використовуючи різні методи спотворення

### Опис

```methodsynopsis
public Imagick::distortImage(int $method, array $arguments, bool $bestfit): bool
```

Спотворює зображення, використовуючи різні методи спотворення, зіставляючи пошукові запити кольору вихідного зображення з новим цільовим зображенням, зазвичай того ж розміру, що й вихідне зображення, якщо для параметра "bestfit" встановлено значення **`true`**

Якщо параметр "bestfit" увімкнений і це дозволяє спотворення, цільове зображення налаштовується таким чином, щоб вихідне зображення повністю відповідало кінцевому цільовому зображенню, яке матиме відповідний розмір та зміщення. Також у багатьох випадках при порівнянні враховуватиметься віртуальне зміщення вихідного зображення.

Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`method`

Метод спотворення зображення. Дивіться [константы искажения](imagick.constants.html#imagick.constants.distortion)

`arguments`

Аргументи обраного методу спотворення.

`bestfit`

Спроба змінити розмір призначення, щоб він відповідав спотвореному джерелу.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::distortImage()****

Спотворення зображення та відображення у браузері.

```php
<?php
/* Создание нового объекта */
$im = new Imagick();

/* Создание нового узора в виде шахматной доски */
$im->newPseudoImage(100, 100, "pattern:checkerboard");

/* Установка формата изображения на png */
$im->setImageFormat('png');

/* Заполнение новых видимых областей прозрачным цветом */
$im->setImageVirtualPixelMethod(Imagick::VIRTUALPIXELMETHOD_TRANSPARENT);

/* Активация матовости */
$im->setImageMatte(true);

/* Контрольные точки для искажения */
$controlPoints = array( 10, 10,
                        10, 5,

                        10, $im->getImageHeight() - 20,
                        10, $im->getImageHeight() - 5,

                        $im->getImageWidth() - 10, 10,
                        $im->getImageWidth() - 10, 20,

                        $im->getImageWidth() - 10, $im->getImageHeight() - 10,
                        $im->getImageWidth() - 10, $im->getImageHeight() - 30);

/* Выполнение искажения */
$im->distortImage(Imagick::DISTORTION_PERSPECTIVE, $controlPoints, true);

/* Вывод изображения */
header("Content-Type: image/png");
echo $im;
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Приклад використання Imagick::distortImage()](images/c0d23d2d6769e53e24a1b3136c064577-distortImage.png)

### Дивіться також

-   [Imagick::blurImage()](imagick.blurimage.html) - Додає фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.html) - Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.html) - Радіальне розмиття зображення