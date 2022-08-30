Клас GMP

-   [« gmpxor](function.gmp-xor.html)
    
-   [GMP::serialize »](gmp.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [GMP](book.gmp.html)
    
-   Клас GMP
    

# Клас GMP

(PHP 5> = 5.6.0, PHP 7, PHP 8)

## Вступ

Номер GMP. Підтримка наступних об'єктів перезавантажена [arithmetic](language.operators.arithmetic.html) [bitwise](language.operators.bitwise.html) і [comparison](language.operators.comparison.html) оператори.

> **Зауваження**
> 
> Об'єктно-орієнтований інтерфейс для маніпуляцій з об'єктами **GMP** Відсутнє. Використовуйте [процедурний GMP API](book.gmp.html)

```classsynopsis

     
    

    
     
      class GMP
     
     {

    /* Методы */
    
   public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [GMP::serialize](gmp.serialize.html) - Серіалізує об'єкт GMP
-   [GMP::unserialize](gmp.unserialize.html) — Десеріалізує параметр data в об'єкті GMP