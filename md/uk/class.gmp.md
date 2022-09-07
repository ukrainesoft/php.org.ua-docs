---
navigation:
  - function.gmp-xor.md: « gmpxor
  - gmp.serialize.md: 'GMP::serialize »'
  - index.md: PHP Manual
  - book.gmp.md: GMP
title: Клас GMP
---
# Клас GMP

(PHP 5> = 5.6.0, PHP 7, PHP 8)

## Вступ

Номер GMP. Підтримка наступних об'єктів перезавантажена [arithmetic](language.operators.arithmetic.md) [bitwise](language.operators.bitwise.md) і [comparison](language.operators.comparison.md) оператори.

> **Зауваження**
> 
> Об'єктно-орієнтований інтерфейс для маніпуляцій з об'єктами **GMP** Відсутнє. Використовуйте [процедурний GMP API](book.gmp.md)

```classsynopsis

     
    

    
     
      class GMP
     
     {

    /* Методы */
    
   public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [GMP::serialize](gmp.serialize.md) - Серіалізує об'єкт GMP
-   [GMP::unserialize](gmp.unserialize.md) — Десеріалізує параметр data в об'єкті GMP
