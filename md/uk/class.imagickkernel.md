---
navigation:
  - imagickpixeliterator.synciterator.md: '« ImagickPixelIterator::syncIterator'
  - imagickkernel.addkernel.md: 'ImagickKernel::addKernel »'
  - index.md: PHP Manual
  - book.imagick.md: ImageMagick
title: Клас ImagickKernel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ImagickKernel

(PECL imagick >= 3.3.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ImagickKernel
     
     {
    

    /* Методы */
    
   public addKernel(ImagickKernel $ImagickKernel): void
public addUnityKernel(float $scale): void
public static fromBuiltin(int $kernelType, string $kernelString): ImagickKernel
public static fromMatrix(array $matrix, array $origin = ?): ImagickKernel
public getMatrix(): array
public scale(float $scale, int $normalizeFlag = ?): void
public separate(): array

   }
```

## Зміст

-   [ImagickKernel::addKernel](imagickkernel.addkernel.md)— Приєднує інше ядро ​​до цього ядра
-   [ImagickKernel::addUnityKernel](imagickkernel.addunitykernel.md)— Додає ядро ​​Unity до списку ядер
-   [ImagickKernel::fromBuiltIn](imagickkernel.frombuiltin.md)— Створює ядро ​​із вбудованого ядра
-   [ImagickKernel::fromMatrix](imagickkernel.frommatrix.md) \- Створює ядро ​​з двовимірної матриці значень
-   [ImagickKernel::getMatrix](imagickkernel.getmatrix.md)— Отримує 2d матрицю значень, що використовуються у цьому ядрі
-   [ImagickKernel::scale](imagickkernel.scale.md) \- Масштабує список ядер на задану величину
-   [ImagickKernel::separate](imagickkernel.separate.md)— Поділяє пов'язаний набір ядер і повертає масив ImagickKernels
