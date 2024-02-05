---
navigation:
  - imagickdraw.setstrokecolor.md: '« ImagickDraw::setStrokeColor'
  - imagickdraw.setstrokedashoffset.md: 'ImagickDraw::setStrokeDashOffset »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeDashArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeDashArray

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeDashArray — Задає патерн зі штрихів та пробілів, які використовуються для обведення контурів

### Опис

```methodsynopsis
public ImagickDraw::setStrokeDashArray(array $dashArray): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає патерн із штрихів та пробілів, який використовується для обведення контурів. strokeDashArray являє собою масив чисел, що визначають довжину штрихів, що чергуються, і пробілів в пікселях. Якщо вказано непарну кількість значень, список значень повторюється, щоб отримати парну кількість значень. Щоб видалити існуючий масив штрихів, потрібно передати number\_elements зі значенням нуль та dash\_array зі значенням null. Типовий масив strokeDashArray\_ може містити елементи 5 3 2.

### Список параметрів

`dashArray`

Масив чисел з плаваючою точкою.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**ImagickDraw::setStrokeDashArray()\*\*\*\*

```php
<?php
function setStrokeDashArray($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(4);

    $draw->setStrokeDashArray([10, 10]);
    $draw->rectangle(100, 50, 225, 175);

    $draw->setStrokeDashArray([20, 5, 20, 5, 5, 5,]);
    $draw->rectangle(275, 50, 400, 175);

    $draw->setStrokeDashArray([20, 5, 20, 5, 5]);
    $draw->rectangle(100, 200, 225, 350);

    $draw->setStrokeDashArray([1, 1, 1, 1, 2, 2, 3, 3, 5, 5, 8, 8, 13, 13, 21, 21, 34, 34, 55, 55, 89, 89, 144, 144, 233, 233, 377, 377, 610, 610, 987, 987, 1597, 1597, 2584, 2584, 4181, 4181,]);

    $draw->rectangle(275, 200, 400, 350);

    $image = new \Imagick();
    $image->newImage(500, 400, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
