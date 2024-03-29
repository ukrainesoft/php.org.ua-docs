---
navigation:
  - imagickdraw.settextundercolor.md: '« ImagickDraw::setTextUnderColor'
  - imagickdraw.setviewbox.md: 'ImagickDraw::setViewbox »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setVectorGraphics'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setVectorGraphics

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setVectorGraphics — Встановлює векторну графіку

### Опис

```methodsynopsis
public ImagickDraw::setVectorGraphics(string $xml): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює векторну графіку, пов'язану із зазначеним об'єктом ImagickDraw. Метод використовується з [ImagickDraw::getVectorGraphics()](imagickdraw.getvectorgraphics.md) як метод збереження стану векторної графіки.

### Список параметрів

`xml`

XML, що містить векторну графіку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setVectorGraphics()\*\*\*\*

```php
<?php
function setVectorGraphics() {
    //Создание объекта для рисования с каким-нибудь рисунком в нём.
    $draw = new \ImagickDraw();
    $draw->setFillColor("red");
    $draw->circle(20, 20, 50, 50);
    $draw->setFillColor("blue");
    $draw->circle(50, 70, 50, 50);
    $draw->rectangle(50, 120, 80, 150);

    //Получение рисунка в виде строки
    $SVG = $draw->getVectorGraphics();

    //$svg - строка, и её можно сохранить везде, где строка может быть сохранена

    //Использование сохранённого рисунка для создания нового объекта для рисования
    $draw2 = new \ImagickDraw();
    //По-видимому, в тексте SVG отсутствует корневой элемент.
    $draw2->setVectorGraphics("<root>".$SVG."</root>");

    $imagick = new \Imagick();
    $imagick->newImage(200, 200, 'white');
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw2);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
