Опис

-   [« ImagickKernel::getMatrix](imagickkernel.getmatrix.html)
    
-   [ImagickKernel::separate »](imagickkernel.separate.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickKernel](class.imagickkernel.html)
    
-   Опис
    

# ImagickKernel::scale

(PECL imagick >= 3.3.0)

ImagickKernel::scale — Опис

### Опис

```methodsynopsis
public ImagickKernel::scale(float $scale, int $normalizeFlag = ?): void
```

ScaleKernelInfo() масштабує заданий список ядер на задану величину з нормалізацією суми значень ядра або без неї (відповідно до заданих прапорів). Точна поведінка функції залежить від типу нормалізації, що використовується, дивіться подробиці на [http://www.imagemagick.org/api/morphology.php#ScaleKernelInfo](http://www.imagemagick.org/api/morphology.php#ScaleKernelInfo). Прапор має бути одним із наступних: Imagick::NORMALIZEKERNELVALUE, Imagick::NORMALIZEKERNELCORRELATE, Imagick::NORMALIZEKERNELPERCENT чи не встановлено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::scale()****

```php
<?php


    function renderKernelTable($matrix) {
        $output = "<table class='infoTable'>";

        foreach ($matrix as $row) {
            $output .= "<tr>";
            foreach ($row as $cell) {
                $output .= "<td style='text-align:left'>";
                if ($cell === false) {
                    $output .= "false";
                }
                else {
                    $output .= round($cell, 3);
                }
                $output .= "</td>";
            }
            $output .= "</tr>";
        }

        $output .= "</table>";

        return $output;
    }


    $output = "";

    $matrix = [
        [-1, 0, -1],
        [ 0, 4,  0],
        [-1, 0, -1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);
    $kernelClone = clone $kernel;

    $output .= "Старт ядра<br/>";
    $output .= renderKernelTable($kernel->getMatrix());


    $output .= "Масштабирование с NORMALIZE_KERNEL_VALUE. The  <br/>";
    $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_VALUE);
    $output .= renderKernelTable($kernel->getMatrix());


    $kernel = clone $kernelClone;
    $output .= "Масштабирование в процентах<br/>";
    $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_PERCENT);
    $output .= renderKernelTable($kernel->getMatrix());

    $matrix2 = [
        [-1, -1, 1],
        [ -1, false,  1],
        [1, 1, 1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix2);
    $output .= "Масштабирование по корреляции<br/>";
    $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_CORRELATE);
    $output .= renderKernelTable($kernel->getMatrix());

    return $output;
?>
```