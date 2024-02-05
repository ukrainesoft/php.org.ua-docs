---
navigation:
  - imagickkernel.getmatrix.md: '« ImagickKernel::getMatrix'
  - imagickkernel.separate.md: 'ImagickKernel::separate »'
  - index.md: PHP Manual
  - class.imagickkernel.md: ImagickKernel
title: 'ImagickKernel::scale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickKernel::scale

(PECL imagick >= 3.3.0)

ImagickKernel::scale — Масштабує список ядер на задану величину

### Опис

```methodsynopsis
public ImagickKernel::scale(float $scale, int $normalizeFlag = ?): void
```

Масштабує заданий список ядер на задану величину з нормалізацією або без нормалізації суми значень ядер (згідно з заданими прапорами). Точна поведінка функції залежить від типу нормалізації, що використовується, дивіться подробиці на [http://www.imagemagick.org/api/morphology.php#ScaleKernelInfo](http://www.imagemagick.org/api/morphology.php#ScaleKernelInfo)

### Список параметрів

`scale`

`normalizeFlag`

-   Imagick::NORMALIZE\_KERNEL\_NONE
-   Imagick::NORMALIZE\_KERNEL\_VALUE
-   Imagick::NORMALIZE\_KERNEL\_CORRELATE
-   Imagick::NORMALIZE\_KERNEL\_PERCENT

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** ImagickKernel::scale()\*\*\*\*

```php
<?php


    function renderKernelTable($matrix) {
        $output = "<table class='infoTable'>";

        foreach ($matrix as $row) {
            $output .= "<tr>";
            foreach ($row as $cell) {
                $output .= "<td style='text-align:left'>";
                if ($cell === false) {
                    $output .= "false";
                }
                else {
                    $output .= round($cell, 3);
                }
                $output .= "</td>";
            }
            $output .= "</tr>";
        }

        $output .= "</table>";

        return $output;
    }


    $output = "";

    $matrix = [
        [-1, 0, -1],
        [ 0, 4,  0],
        [-1, 0, -1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);
    $kernelClone = clone $kernel;

    $output .= "Старт ядра<br/>";
    $output .= renderKernelTable($kernel->getMatrix());


    $output .= "Масштабирование с NORMALIZE_KERNEL_VALUE. The  <br/>";
    $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_VALUE);
    $output .= renderKernelTable($kernel->getMatrix());


    $kernel = clone $kernelClone;
    $output .= "Масштабирование в процентах<br/>";
    $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_PERCENT);
    $output .= renderKernelTable($kernel->getMatrix());

    $matrix2 = [
        [-1, -1, 1],
        [ -1, false,  1],
        [1, 1, 1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix2);
    $output .= "Масштабирование по корреляции<br/>";
    $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_CORRELATE);
    $output .= renderKernelTable($kernel->getMatrix());

    return $output;
?>
```
