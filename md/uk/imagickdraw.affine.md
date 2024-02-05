---
navigation:
  - class.imagickdraw.md: « ImagickDraw
  - imagickdraw.annotation.md: 'ImagickDraw::annotation »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::affine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::affine

(PECL imagick 2, PECL imagick 3)

ImagickDraw::affine — Регулює поточну матрицю афінного перетворення

### Опис

```methodsynopsis
public ImagickDraw::affine(array $affine): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Коригує поточну матрицю афінного перетворення із зазначеною матрицею афінного перетворення.

### Список параметрів

`affine`

Параметри афінної матриці

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::affine()\*\*\*\*

```php
<?php
function affine($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeWidth(1);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);

    $PI = 3.141592653589794;
    $angle = 60 * $PI / 360;

    //Масштабирование координат чертежа.
    $affineScale = array("sx" => 1.75, "sy" => 1.75, "rx" => 0, "ry" => 0, "tx" => 0, "ty" => 0);

    //Сдвиг координат чертежа.
    $affineShear = array("sx" => 1, "sy" => 1, "rx" => sin($angle), "ry" => -sin($angle), "tx" => 0, "ty" => 0);

    //Поворот координат чертежа. Аффинная матрица сдвига даёт
    //неправильно масштабированные чертежи.
    $affineRotate = array("sx" => cos($angle), "sy" => cos($angle), "rx" => sin($angle), "ry" => -sin($angle), "tx" => 0, "ty" => 0,);

    //Смещение рисунка
    $affineTranslate = array("sx" => 1, "sy" => 1, "rx" => 0, "ry" => 0, "tx" => 30, "ty" => 30);

    //Единичная аффинная матрица
    $affineIdentity = array("sx" => 1, "sy" => 1, "rx" => 0, "ry" => 0, "tx" => 0, "ty" => 0);

    $examples = [$affineScale, $affineShear, $affineRotate, $affineTranslate, $affineIdentity,];

    $count = 0;

    foreach ($examples as $example) {
        $draw->push();
        $draw->translate(($count % 2) * 250, intval($count / 2) * 250);
        $draw->translate(100, 100);
        $draw->affine($example);
        $draw->rectangle(-50, -50, 50, 50);
        $draw->pop();
        $count++;
    }

    //Создание объекта изображения, в который можно преобразовать команды рисования.
    $image = new \Imagick();
    $image->newImage(500, 750, $backgroundColor);
    $image->setImageFormat("png");

    //Преобразование команд рисования в объекте ImagickDraw
    //в изображение.
    $image->drawImage($draw);

    //Отображение изображения в браузере
    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
