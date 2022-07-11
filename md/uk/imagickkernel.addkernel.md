- [«ImagickKernel](class.imagickkernel.md)
- [ImagickKernel::addUnityKernel »](imagickkernel.addunitykernel.md)

- [PHP Manual](index.md)
- [ImagickKernel](class.imagickkernel.md)
- Опис

# ImagickKernel::addKernel

(PECL imagick \>= 3.3.0)

ImagickKernel::addKernel — Опис

### Опис

public
**ImagickKernel::addKernel**([ImagickKernel](class.imagickkernel.md)
`$ImagickKernel`): void

Приєднує інше ядро до цього ядра, щоб дозволити їм обом
застосовуватися в одній морфології чи функції фільтра. Повертає нове
об'єднане ядро.

### Список параметрів

`ImagickKernel`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::addKernel()****

` <?phpfunction addKernel($imagePath) {    $matrix1 = [        [-1, -1, -1],        [ 0,  0,  0],        [ 1,  1,  1],    ]; $matrix2 = [-1, |-1,  , 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1; $kernel1==ImagickKernel::fromMatrix($matrix1); $kernel2=ImagickKernel::fromMatrix($matrix2); $kernel1->addKernel($kernel2); $imagick = new \Imagick(realpath($imagePath)); $imagick->filter($kernel1); header("Content-Type: image/jpg"); echo $imagick->getImageBlob();}?> `
