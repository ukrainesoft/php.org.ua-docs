---
navigation:
  - random-engine-secure.generate.md: '« Random\\Engine\\Secure::generate'
  - random-engine-mt19937.construct.md: 'Random\\Engine\\Mt19937::\_\_construct »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\Engine\\Mt19937
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\Engine\\Mt19937

(PHP 8 >= 8.2.0)

## Вступ

Реалізує алгоритм [» Mt19937](http://www.math.sci.hiroshima-u.ac.jp/m-mat/MT/ARTICLES/mt.pdf) ("Mersenne Twister").

## Огляд класів

```classsynopsis

    
     final
     class Random\Engine\Mt19937
    

    
     implements
      Random\Engine {

    /* Методы */
    
   public __construct(?int $seed = null, int $mode = MT_RAND_MT19937)

    public __debugInfo(): array
public generate(): string
public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [Random\\Engine\\Mt19937::\_\_construct](random-engine-mt19937.construct.md) \- Створює новий об'єкт двигуна Mt19937
-   [Random\\Engine\\Mt19937::\_\_debugInfo](random-engine-mt19937.debuginfo.md) \- Повертає внутрішній стан двигуна
-   [Random\\Engine\\Mt19937::generate](random-engine-mt19937.generate.md)— Створює 32 біти випадкової послідовності
-   [Random\\Engine\\Mt19937::\_\_serialize](random-engine-mt19937.serialize.md)— Серіалізує об'єкт Mt19937
-   [Random\\Engine\\Mt19937::\_\_unserialize](random-engine-mt19937.unserialize.md) \- Десеріалізує параметр data в об'єкт Mt19937
