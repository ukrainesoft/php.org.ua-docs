---
navigation:
  - imagickkernel.scale.md: '« ImagickKernel::scale'
  - refs.remote.mail.md: Модулі для роботи з поштою
  - index.md: PHP Manual
  - class.imagickkernel.md: ImagickKernel
title: 'ImagickKernel::separate'
---
# ImagickKernel::separate

(PECL imagick >= 3.3.0)

ImagickKernel::separate — Опис

### Опис

```methodsynopsis
public ImagickKernel::separate(): array
```

Розділяє пов'язаний набір ядер і повертає масив ImagickKernels.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::separate()****

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


    $matrix = [
        [-1, 0, -1],
        [ 0, 4,  0],
        [-1, 0, -1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);
    $kernel->scale(4, \Imagick::NORMALIZE_KERNEL_VALUE);
    $diamondKernel = \ImagickKernel::fromBuiltIn(
        \Imagick::KERNEL_DIAMOND,
        "2"
    );

    $kernel->addKernel($diamondKernel);

    $kernelList = $kernel->separate();

    $output = '';
    $count = 0;
    foreach ($kernelList as $kernel) {
        $output .= "<br/>Ядро $count<br/>";
        $output .= renderKernelTable($kernel->getMatrix());
        $count++;
    }

    return $output;

?>
```
