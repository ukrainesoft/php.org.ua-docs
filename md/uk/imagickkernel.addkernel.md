---
navigation:
  - class.imagickkernel.md: « ImagickKernel
  - imagickkernel.addunitykernel.md: 'ImagickKernel::addUnityKernel »'
  - index.md: PHP Manual
  - class.imagickkernel.md: ImagickKernel
title: 'ImagickKernel::addKernel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickKernel::addKernel

(PECL imagick >= 3.3.0)

ImagickKernel::addKernel — Приєднує інше ядро ​​до цього ядра

### Опис

```methodsynopsis
public ImagickKernel::addKernel(ImagickKernel $ImagickKernel): void
```

Приєднує інше ядро ​​до цього ядра, щоб дозволити їм обом застосовуватися в одній морфології або функції фільтра. Повертає нове об'єднане ядро.

### Список параметрів

`ImagickKernel`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** ImagickKernel::addKernel()\*\*\*\*

```php
<?php
function addKernel($imagePath) {
    $matrix1 = [
        [-1, -1, -1],
        [ 0,  0,  0],
        [ 1,  1,  1],
    ];

    $matrix2 = [
        [-1,  0,  1],
        [-1,  0,  1],
        [-1,  0,  1],
    ];

    $kernel1 = ImagickKernel::fromMatrix($matrix1);
    $kernel2 = ImagickKernel::fromMatrix($matrix2);
    $kernel1->addKernel($kernel2);

    $imagick = new \Imagick(realpath($imagePath));
    $imagick->filter($kernel1);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();

}

?>
```
