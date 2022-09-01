---
navigation:
  - imagickpixeliterator.synciterator.md: '« ImagickPixelIterator::syncIterator'
  - imagickkernel.addkernel.md: 'ImagickKernel::addKernel »'
  - index.md: PHP Manual
  - book.imagick.md: ImageMagick
title: Клас ImagickKernel
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

-   [ImagickKernel::addKernel](imagickkernel.addkernel.md) - Опис
-   [ImagickKernel::addUnityKernel](imagickkernel.addunitykernel.md) - Опис
-   [ImagickKernel::fromBuiltIn](imagickkernel.frombuiltin.md) - Опис
-   [ImagickKernel::fromMatrix](imagickkernel.frommatrix.md) - Опис
-   [ImagickKernel::getMatrix](imagickkernel.getmatrix.md) - Опис
-   [ImagickKernel::scale](imagickkernel.scale.md) - Опис
-   [ImagickKernel::separate](imagickkernel.separate.md) - Опис
