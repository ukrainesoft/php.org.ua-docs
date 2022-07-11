- [« ImagickKernel::getMatrix](imagickkernel.getmatrix.md)
- [ImagickKernel::separate »](imagickkernel.separate.md)

- [PHP Manual](index.md)
- [ImagickKernel](class.imagickkernel.md)
- Опис

# ImagickKernel::scale

(PECL imagick \>= 3.3.0)

ImagickKernel::scale — Опис

### Опис

public **ImagickKernel::scale**(float `$scale`, int `$normalizeFlag` =
?): void

ScaleKernelInfo() масштабує заданий список ядер на задану
величину, з нормалізацією суми значень ядра або без неї (у
відповідно до заданих прапорів). Точна поведінка функції залежить від
використовуваного типу нормалізації, дивіться подробиці на
http://www.imagemagick.org/api/morphology.php#ScaleKernelInfo. Прапор
повинен бути одним з наступних: Imagick::NORMALIZE_KERNEL_VALUE,
Imagick::NORMALIZE_KERNEL_CORRELATE, Imagick::NORMALIZE_KERNEL_PERCENT
або не встановлено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::scale()****

` <?php    function renderKernelTable($matrix) {        $output = "<table class='infoTable'>"; foreach ($matrix as $row) {            $output .= "<tr>"; foreach ($row as $cell) {                $output .= "<td style='text-align:left'>"; if ($cell ====false) {                    $output .= "false"; }                 else {                     $output .= round($cell, }                  $output .= "</td>"; }             $output .= "</tr>"; }        $output .= "</table>"; return $output; }    $output = ""; $matrix = [        [-1, 0, -1],       [ 0, 4,  0],         [-1, , ; $kernel= \ImagickKernel::fromMatrix($matrix); $kernelClone = clone $kernel; $output .= "Старт ядра<br/>"; $output.==renderKernelTable($kernel->getMatrix()); $output .= "Масштабування з NORMALIZE_KERNEL_VALUE. The  <br/>"; $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_VALUE); $output.==renderKernelTable($kernel->getMatrix()); $kernel= clone $kernelClone; $output .= "Масштабування в відсотках<br/>"; $kernel->scale(2, \Imagick::NORMALIZE_KERNEL_PERCENT); $output.==renderKernelTable($kernel->getMatrix()); $matrix2 = [        [-1, -1, 1],        [ -1, false,  1],        [1, ,| $kernel= \ImagickKernel::fromMatrix($matrix2); $output .= "Масштабування по кореляції<br/>"; $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_CORRELATE); $output.==renderKernelTable($kernel->getMatrix()); return $output;?> `
