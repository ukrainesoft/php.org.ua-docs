Перевірити різницю між цим кольором та іншим

-   [« ImagickPixel::isPixelSimilarQuantum](imagickpixel.ispixelsimilarquantum.md)
    
-   [ImagickPixel::setColor »](imagickpixel.setcolor.md)
    
-   [PHP Manual](index.md)
    
-   [ImagickPixel](class.imagickpixel.md)
    
-   Перевірити різницю між цим кольором та іншим
    

# ImagickPixel::isSimilar

(PECL imagick 2, PECL imagick 3)

ImagickPixel::isSimilar — Перевірити різницю між цим кольором та іншим

### Опис

```methodsynopsis
public ImagickPixel::isSimilar(ImagickPixel $color, float $fuzz): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Перевіряється різниця кольору, описаного поточним об'єктом ImagickPixel та кольору в переданому об'єкті, шляхом побудови їх RGB значень у колірному кубі. Якщо різниця між ними менша за передане fuzz-значення, то кольори вважаються однаковими. Застарів на користь [ImagickPixel::isPixelSimilar()](imagickpixel.ispixelsimilar.md)

### Список параметрів

`color`

Об'єкт ImagickPixel можна порівняти з поточним об'єктом.

`fuzz`

Максимальна різниця, за якої кольори вважатимуться однаковими. Теоретичним максимумом цього значення вважатимуться квадратний корінь із трьох (1.732).

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickPixel::isSimilar()****

```php
<?php
        // Тесты ниже написаны с учётом максимальной дистанции 255
        // следовательно мы должны масштабировать их на корень из 3 - длину диагонали
        // единичного куба
        $root3 = 1.732050807568877;

        $tests = array(
            ['rgb(245, 0, 0)',      'rgb(255, 0, 0)',   9 / $root3,         false,],
            ['rgb(245, 0, 0)',      'rgb(255, 0, 0)',  10 / $root3,         true,],
            ['rgb(0, 0, 0)',        'rgb(7, 7, 0)',     9 / $root3,         false,],
            ['rgb(0, 0, 0)',        'rgb(7, 7, 0)',    10 / $root3,         true,],
            ['rgba(0, 0, 0, 1)',    'rgba(7, 7, 0, 1)', 9 / $root3,         false,],
            ['rgba(0, 0, 0, 1)',    'rgba(7, 7, 0, 1)',    10 / $root3,     true,],
            ['rgb(128, 128, 128)',  'rgb(128, 128, 120)',   7 / $root3,     false,],
            ['rgb(128, 128, 128)',  'rgb(128, 128, 120)',   8 / $root3,     true,],
            ['rgb(0, 0, 0)',        'rgb(255, 255, 255)',   254.9,          false,],
            ['rgb(0, 0, 0)',        'rgb(255, 255, 255)',   255,            true,],
            ['rgb(255, 0, 0)',      'rgb(0, 255, 255)',     254.9,          false,],
            ['rgb(255, 0, 0)',      'rgb(0, 255, 255)',     255,            true,],
            ['black',               'rgba(0, 0, 0)',        0.0,            true],
            ['black',               'rgba(10, 0, 0, 1.0)',  10.0 / $root3,  true],);

        $output = "<table width='100%' class='infoTable'><thead>
                <tr>
                <th>
                Color 1
                </th>
                <th>
                Color 2
                </th>
                <th>
                    Тестовая дистанция * 255
                </th>
                <th>
                    Есть в пределах досягаемости
                </th>
                </tr>
        </thead>";

        $output .= "<tbody>";

        foreach ($tests as $testInfo) {
            $color1 = $testInfo[0];
            $color2 = $testInfo[1];
            $distance = $testInfo[2];
            $expectation = $testInfo[3];
            $testDistance = ($distance / 255.0);

            $color1Pixel = new \ImagickPixel($color1);
            $color2Pixel = new \ImagickPixel($color2);

            $isSimilar = $color1Pixel->isPixelSimilar($color2Pixel, $testDistance);


            if ($isSimilar !== $expectation) {
                echo "Тест дистанции провален. Цвет [$color1] в сравнении с [$color2] не попадает в дистанцию $testDistance.".NL;
            }

            $layout = "<tr>
                <td>%s</td>
                <td>%s</td>
                <td>%s</td>
                <td style='text-align: center;'>%s</td>
            </tr>";

            $output .= sprintf(
                $layout,
                $color1,
                $color2,
                $distance,
                $isSimilar ? 'да' : 'нет'
            );
        }

        $output .= "</tbody></table>";

        return $output;

?>
```