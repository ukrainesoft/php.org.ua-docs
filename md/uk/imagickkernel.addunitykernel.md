- [« ImagickKernel::addKernel](imagickkernel.addkernel.md)
- [ImagickKernel::fromBuiltIn »](imagickkernel.frombuiltin.md)

- [PHP Manual](index.md)
- [ImagickKernel](class.imagickkernel.md)
- Опис

# ImagickKernel::addUnityKernel

(PECL imagick \>= 3.3.0)

ImagickKernel::addUnityKernel — Опис

### Опис

public **ImagickKernel::addUnityKernel**(float `$scale`): void

Додає вказану кількість згорткового ядра 'Unity' до вказаного
попередньо масштабованому та нормалізованому ядру. Це фактично
додає ту кількість вихідного зображення в ядро, що виходить
згортки. В результаті виходить перетворення певних ядер на
змішані м'які плями, нерізкі ядра або загострені ядра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::addUnityKernel()****

` <?php    function renderKernelTable($matrix) {        $output = "<table class='infoTable'>"; foreach ($matrix as $row) {            $output .= "<tr>"; foreach ($row as $cell) {                $output .= "<td style='text-align:left'>"; if ($cell ====false) {                    $output .= "false"; }                 else {                     $output .= round($cell, }                  $output .= "</td>"; }             $output .= "</tr>"; }        $output .= "</table>"; return $output; }   $matrix = [        [-1, 0, -1],        [ 0, 4,  0], | $kernel= \ImagickKernel::fromMatrix($matrix); $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_VALUE); $output = "Перед додаваннямunity ядра: <br/>"; $output.==renderKernelTable($kernel->getMatrix()); $kernel->addUnityKernel(0.5); $output .= "Після додавання unity ядра: <br/>"; $output.==renderKernelTable($kernel->getMatrix()); $kernel->scale(1, \Imagick::NORMALIZE_KERNEL_VALUE); $output .= "Після перенормування ядра: <br/>"; $output.==renderKernelTable($kernel->getMatrix()); echo $output;?> `

**Приклад #2 Приклад використання **ImagickKernel::addUnityKernel()****

<-phpfunction AddUnityKernel($imagePath) {- ,  ,   ,                 $kernel= ImagickKernel::fromMatrix($matrix); $kernel->scale(4, \Imagick::NORMALIZE_KERNEL_VALUE); $kernel->addUnityKernel(0.5); $imagick = new \Imagick(realpath($imagePath)); $imagick->filter($kernel); header("Content-Type: image/jpg"); echo $imagick->getImageBlob();}?> `
