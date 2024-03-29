---
navigation:
  - imagick.displayimages.md: '« Imagick::displayImages'
  - imagick.drawimage.md: 'Imagick::drawImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::distortImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::distortImage

(PECL imagick 2 >= 2.0.1, PECL imagick 3)

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

Метод искажения изображения. Смотрите[константи спотворення](imagick.constants.md#imagick.constants.distortion)

`arguments`

Аргументи обраного методу спотворення.

`bestfit`

Спроба змінити розмір призначення, щоб він відповідав спотвореному джерелу.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::distortImage()\*\* :\*\*

Спотворення зображення та відображення у браузері.

```php
<?php
/* Создание нового объекта */
$im = new Imagick();

/* Создание нового узора в виде шахматной доски */
$im->newPseudoImage(100, 100, "pattern:checkerboard");

/* Установка формата изображения на png */
$im->setImageFormat('png');

/* Заполнение новых видимых областей прозрачным цветом */
$im->setImageVirtualPixelMethod(Imagick::VIRTUALPIXELMETHOD_TRANSPARENT);

/* Активация матовости */
$im->setImageMatte(true);

/* Контрольные точки для искажения */
$controlPoints = array( 10, 10,
                        10, 5,

                        10, $im->getImageHeight() - 20,
                        10, $im->getImageHeight() - 5,

                        $im->getImageWidth() - 10, 10,
                        $im->getImageWidth() - 10, 20,

                        $im->getImageWidth() - 10, $im->getImageHeight() - 10,
                        $im->getImageWidth() - 10, $im->getImageHeight() - 30);

/* Выполнение искажения */
$im->distortImage(Imagick::DISTORTION_PERSPECTIVE, $controlPoints, true);

/* Вывод изображения */
header("Content-Type: image/png");
echo $im;
?>
```

Висновок наведеного прикладу буде схожим на:

![Приклад використання Imagick::distortImage()](images/c0d23d2d6769e53e24a1b3136c064577-distortImage.png)

### Дивіться також

-   [Imagick::blurImage()](imagick.blurimage.md) \- Додає фільтр розмиття до зображення
-   [Imagick::motionBlurImage()](imagick.motionblurimage.md) \- Імітує розмиття у русі
-   [Imagick::radialBlurImage()](imagick.radialblurimage.md) \- Радіальне розмиття зображення
