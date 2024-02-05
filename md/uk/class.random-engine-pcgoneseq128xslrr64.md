---
navigation:
  - random-engine-mt19937.unserialize.md: '« Random\\Engine\\Mt19937::\_\_unserialize'
  - random-engine-pcgoneseq128xslrr64.construct.md: 'Random\\Engine\\PcgOneseq128XslRr64::\_\_construct »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\Engine\\PcgOneseq128XslRr64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\Engine\\PcgOneseq128XslRr64

(PHP 8 >= 8.2.0)

## Вступ

Реалізує [» перестановний конгруентний генератор (PCG)](https://www.pcg-random.org/) зі 128 бітами стану, перетвореннями XSL і RR та 64 бітами на виході.

## Огляд класів

```classsynopsis

    
     final
     class Random\Engine\PcgOneseq128XslRr64
    

    
     implements
      Random\Engine {

    /* Методы */
    
   public __construct(string|int|null $seed = null)

    public __debugInfo(): array
public generate(): string
public jump(int $advance): void
public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [Random\\Engine\\PcgOneseq128XslRr64::\_\_construct](random-engine-pcgoneseq128xslrr64.construct.md) \- Створює новий двигун PCG Oneseq 128 XSL RR 64
-   [Random\\Engine\\PcgOneseq128XslRr64::\_\_debugInfo](random-engine-pcgoneseq128xslrr64.debuginfo.md) \- Повертає внутрішній стан двигуна
-   [Random\\Engine\\PcgOneseq128XslRr64::generate](random-engine-pcgoneseq128xslrr64.generate.md)— Створює 64 біти випадкової послідовності
-   [Random\\Engine\\PcgOneseq128XslRr64::jump](random-engine-pcgoneseq128xslrr64.jump.md) \- Ефективне переміщення двигуна вперед на кілька кроків
-   [Random\\Engine\\PcgOneseq128XslRr64::\_\_serialize](random-engine-pcgoneseq128xslrr64.serialize.md)— Серіалізує об'єкт PcgOneseq128XslRr64
-   [Random\\Engine\\PcgOneseq128XslRr64::\_\_unserialize](random-engine-pcgoneseq128xslrr64.unserialize.md)— Десеріалізує параметр data в об'єкт PcgOneseq128XslRr64
