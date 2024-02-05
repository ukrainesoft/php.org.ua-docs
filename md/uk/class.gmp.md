---
navigation:
  - function.gmp-xor.md: « gmp\_xor
  - gmp.construct.md: 'GMP::\_\_construct »'
  - index.md: PHP Manual
  - book.gmp.md: GMP
title: Клас GMP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас GMP

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

## Вступ

Номер GMP. Ці об'єкти підтримують навантаження наступних операторів: [арифметичних](language.operators.arithmetic.md) [побітових](language.operators.bitwise.md) і [порівняння](language.operators.comparison.md)

> **Зауваження** :
> 
> Немає об'єктно-орієнтованого інтерфейсу для керування об'єктами **GMP**. Для керування такими об'єктами рекомендовано використовувати [процедурний GMP API](book.gmp.md)

```classsynopsis

    
     class GMP
     {

    /* Методы */
    
   public __construct(int|string $num = 0, int $base = 0)

    public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [GMP::\_\_construct](gmp.construct.md) \- Створює GMP-число
-   [GMP::\_\_serialize](gmp.serialize.md) \- Серіалізує об'єкт GMP
-   [GMP::\_\_unserialize](gmp.unserialize.md)— Десеріалізує параметр data в об'єкті GMP
