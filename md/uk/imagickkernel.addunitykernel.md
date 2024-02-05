---
navigation:
  - imagickkernel.addkernel.md: '« ImagickKernel::addKernel'
  - imagickkernel.frombuiltin.md: 'ImagickKernel::fromBuiltIn »'
  - index.md: PHP Manual
  - class.imagickkernel.md: ImagickKernel
title: 'ImagickKernel::addUnityKernel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickKernel::addUnityKernel

(PECL imagick >= 3.3.0)

ImagickKernel::addUnityKernel — Додає ядро ​​Unity до списку ядер

### Опис

```methodsynopsis
public ImagickKernel::addUnityKernel(float $scale): void
```

Додає зазначену кількість згорткового ядра 'Unity' до зазначеного попередньо масштабованого та нормалізованого ядра. Це фактично додає ту кількість вихідного зображення в ядро ​​згортки, що виходить. В результаті виходить перетворення певних ядер у змішані м'які плями, нерізкі ядра або загострені ядра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**ImagickKernel::addUnityKernel()\*\*\*\*

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

    $matrix = [
        [-1, 0, -1],
        [ 0, 4,  0],
        [-1, 0, -1],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);
    $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_VALUE);
    $output = "Перед добавлением unity ядра: <br/>";
    $output .= renderKernelTable($kernel->getMatrix());
    $kernel->addUnityKernel(0.5);
    $output .= "После добавления unity ядра: <br/>";
    $output .= renderKernelTable($kernel->getMatrix());


    $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_VALUE);
    $output .= "После перенормировки ядра: <br/>";
    $output .= renderKernelTable($kernel->getMatrix());

    echo $output;

?>
```

**Пример #2 Пример использования**ImagickKernel::addUnityKernel()\*\*\*\*

```php
<?php
function addUnityKernel($imagePath) {

    $matrix = [
        [-1, 0, -1],
        [ 0, 4,  0],
        [-1, 0, -1],
    ];

    $kernel = ImagickKernel::fromMatrix($matrix);

    $kernel->scale(4, \Imagick::NORMALIZE_KERNEL_VALUE);
    $kernel->addUnityKernel(0.5);


    $imagick = new \Imagick(realpath($imagePath));
    $imagick->filter($kernel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();

}

?>
```
