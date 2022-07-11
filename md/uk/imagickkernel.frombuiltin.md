- [« ImagickKernel::addUnityKernel](imagickkernel.addunitykernel.md)
- [ImagickKernel::fromMatrix »](imagickkernel.frommatrix.md)

- [PHP Manual](index.md)
- [ImagickKernel](class.imagickkernel.md)
- Опис

# ImagickKernel::fromBuiltIn

(PECL imagick \>= 3.3.0)

ImagickKernel::fromBuiltIn — Опис

### Опис

public static **ImagickKernel::fromBuiltin**(int `$kernelType`, string
`$kernelString`): [ImagickKernel](class.imagickkernel.md)

Створює ядро із вбудованого ядра. Дивіться приклади
http://www.imagemagick.org/Usage/morphology/#kernel. В даний час
символи "обертання" не підтримуються. Приклад: $diamondKernel =
ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DIAMOND, "2");

### Список параметрів

`kerneltype`
Тип ядра для складання, наприклад \Imagick::KERNEL_DIAMOND

`kernelString`
Рядок, що описує параметри, наприклад, "4,2.5"

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::fromBuiltin()****

` <?phpfunction renderKernel(ImagickKernel $imagickKernel) {    $matrix = $imagickKernel->getMatrix(); $imageMargin = 20; $ tileSize = 20; $tileSpace = 4; $shadowSigma==4; $shadowDropX = 20; $shadowDropY = 0; $radius = ($tileSize / 2) * 0.9; $rows==count($matrix); $columns = count($matrix[0]); $imagickDraw= new \ImagickDraw(); $imagickDraw->setFillColor('#afafaf'); $imagickDraw->setStrokeColor('none'); $imagickDraw->translate($imageMargin, $imageMargin); $imagickDraw->push(); ksort($matrix); foreach ($matrix as $row) {        ksort($row); $imagickDraw->push(); foreach ($row as $cell) {             if ($cell !== false) {                    $colorString = sprintf("rgb(%f, %f, %f)", $color, $color, $color); $imagickDraw->setFillColor($colorString); $imagickDraw->rectangle(0, 0, $tileSize, $tileSize); }             $imagickDraw->translate(($tileSize + $tileSpace), 0); }        $imagickDraw->pop(); $imagickDraw->translate(0, ($tileSize + $tileSpace)); }   $imagickDraw->pop(); $width = ($columns * $tileSize) + (($columns - 1) * $tileSpace); $height = ($rows * $tileSize) + (($rows - 1) * $tileSpace); $imagickDraw->push(); $imagickDraw->translate($width/2 , $height/2); $imagickDraw->setFillColor('rgba(0, 0, 0, 0)'); $imagickDraw->setStrokeColor('white'); $imagickDraw->circle(0, 0, $radius - 1, 0); $imagickDraw->setStrokeColor('black'); $imagickDraw->circle(0, 0, $radius, 0); $imagickDraw->pop(); $canvasWidth==$width + (2 * $imageMargin); $canvasHeight = $height + (2 * $imageMargin); $kernel==newImagick(); $kernel->newPseudoImage($  canvasWidth,       $canvasHeight,        'canvas:none'    ); $kernel->setImageFormat('png'); $kernel->drawImage($imagickDraw); /* створення тіні на власному шарі */    $canvas = $kernel->clone(); $canvas->setImageBackgroundColor(new \ImagickPixel('rgb(0, 0, 0)')); $canvas->shadowImage(100, $shadowSigma, $shadowDropX, $shadowDropY); $canvas->setImagePage($canvasWidth, $canvasHeight, -5, -5); $canvas->cropImage($canvasWidth, $canvasHeight, 0, 0); /* накладає вихідний text_layer на shadow_layer */    $canvas->compositeImage($kernel, \Imagick::COMPOSITE_OVER, 0, 0); $canvas->setImageFormat('png'); return $canvas;}function createFromBuiltin($kernelType, $kernelFirstTerm, $kernelSecondTerm, $kernelThirdTerm) {   $string = ''; if ($kernelFirstTerm != false && strlen(trim($kernelFirstTerm)) != 0) {        $string .= $kernelFirstTerm; if ($kernelSecondTerm != false && strlen(trim($kernelSecondTerm)) != 0) {            $string .= ','.$kernelSecon if ($kernelThirdTerm != false && strlen(trim($kernelThirdTerm)) != 0) {                 $string .= '; }        }    }}   $kernel = ImagickKernel::fromBuiltIn(       $kernelType,                                               —————————— return $kernel;}function fromBuiltin($kernelType, $kernelFirstTerm, $kernelSecondTerm, $kernelThirdTerm) {   $diamondKernel = createFromBuiltin($kernel,Ternel $imagick==renderKernel($diamondKernel); header("Content-Type: image/png"); echo $imagick->getImageBlob();}fromBuiltin(\Imagick::KERNEL_DIAMOND, 2, false, false);?> `
