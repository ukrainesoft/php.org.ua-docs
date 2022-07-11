- [« ImagickPixel::setColorValueQuantum](imagickpixel.setcolorvaluequantum.md)
- [ImagickPixel::setIndex »](imagickpixel.setindex.md)

- [PHP Manual](index.md)
- [ImagickPixel](class.imagickpixel.md)
- Установка нормалізованого HSL кольору

# ImagickPixel::setHSL

(PECL imagick 2, PECL imagick 3)

ImagickPixel::setHSL — Встановлення нормалізованого кольору HSL

### Опис

public **ImagickPixel::setHSL**(float `$hue`, float `$saturation`, float
`$luminosity`): bool

Встановлює колір в об'єкті ImagickPixel, використовуючи нормалізовані
значення відтінку, насиченості та яскравості.

### Список параметрів

`hue`
Нормалізоване значення відтінку, як значення кругової веселки (між
0 та 1), де нульовим значенням буде червоний колір.

`saturation`
Нормалізоване значення насиченості, де означає повне насичення.

`luminosity`
Нормалізоване значення яскравості, за шкалою від 0 (чорний) до 1 (білий),
при встановленому HS значення 0.5.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **ImagickPixel::setHSL()****

` <?php//Створення майже чистого червоного кольору$color = new ImagickPixel('rgb(90%, 10%, 10%)');//Отримання значень HSL$colorInfo = $color-> Поворачиваем оттенок на 180 градусов$newHue = $colorInfo['hue'] + 0.5;if ($newHue > 1) {    $newHue = $newHue - 1;}//Устанавливаем ImagickPixel в новый цвет$colorInfo = $color->setHSL ($newHue, $colorInfo['saturation'], $colorInfo['luminosity']);//Перевіряємо, що новий колір є блакитним/зеленим$colorInfo = $color->getcolor();print_r($or > `

Результат виконання цього прикладу:

Array
(
[r] => 26
[g] => 230
[b] => 230
[a] => 255
)

### Примітки

> **Примітка**:
>
> Доступно з версії 6.2.9 та вище бібліотеки ImageMagick.
