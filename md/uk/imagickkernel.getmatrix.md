Опис

-   [« ImagickKernel::fromMatrix](imagickkernel.frommatrix.md)
    
-   [ImagickKernel::scale »](imagickkernel.scale.md)
    
-   [PHP Manual](index.md)
    
-   [ImagickKernel](class.imagickkernel.md)
    
-   Опис
    

# ImagickKernel::getMatrix

(PECL imagick >= 3.3.0)

ImagickKernel::getMatrix — Опис

### Опис

```methodsynopsis
public ImagickKernel::getMatrix(): array
```

Отримати 2d матрицю значень, що використовуються у цьому ядрі. Елементи є або числом з плаваючою точкою для елементів, або 'false', якщо елемент повинен бути пропущений.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Матриця (2d масив) значень, які представляють ядро.

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::getMatrix()****

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

    $output = "Имя встроенного ядра 'ring' с параметрами '2,3.5':<br/>";
    $kernel = \ImagickKernel::fromBuiltIn(
        \Imagick::KERNEL_RING,
        "2,3.5"
    );
    $matrix = $kernel->getMatrix();
    $output .= renderKernelTable($matrix);

    echo $output;

?>
```