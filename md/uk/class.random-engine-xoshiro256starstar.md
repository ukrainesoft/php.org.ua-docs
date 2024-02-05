---
navigation:
  - random-engine-pcgoneseq128xslrr64.unserialize.md: '« Random\\Engine\\PcgOneseq128XslRr64::\_\_unserialize'
  - random-engine-xoshiro256starstar.construct.md: 'Random\\Engine\\Xoshiro256StarStar::\_\_construct »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\Engine\\Xoshiro256StarStar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\Engine\\Xoshiro256StarStar

(PHP 8 >= 8.2.0)

## Вступ

Реалізує алгоритм [» xoshiro256\*\*](https://prng.di.unimi.it/)

## Огляд класів

```classsynopsis

    
     final
     class Random\Engine\Xoshiro256StarStar
    

    
     implements
      Random\Engine {

    /* Методы */
    
   public __construct(string|int|null $seed = null)

    public __debugInfo(): array
public generate(): string
public jump(): void
public jumpLong(): void
public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [Random\\Engine\\Xoshiro256StarStar::\_\_construct](random-engine-xoshiro256starstar.construct.md) \- Створює новий об'єкт двигуна xoshiro256\*\*
-   [Random\\Engine\\Xoshiro256StarStar::\_\_debugInfo](random-engine-xoshiro256starstar.debuginfo.md) \- Повертає внутрішній стан двигуна
-   [Random\\Engine\\Xoshiro256StarStar::generate](random-engine-xoshiro256starstar.generate.md)— Генерує 64 біти випадкової послідовності
-   [Random\\Engine\\Xoshiro256StarStar::jump](random-engine-xoshiro256starstar.jump.md) \- Ефективно переміщає двигун вперед на 2^128 кроків
-   [Random\\Engine\\Xoshiro256StarStar::jumpLong](random-engine-xoshiro256starstar.jumplong.md) \- Ефективно переміщає двигун вперед на 2^192 кроки
-   [Random\\Engine\\Xoshiro256StarStar::\_\_serialize](random-engine-xoshiro256starstar.serialize.md) \- Серіалізує об'єкт Xoshiro256StarStar
-   [Random\\Engine\\Xoshiro256StarStar::\_\_unserialize](random-engine-xoshiro256starstar.unserialize.md)— Десеріалізує параметр data в об'єкті Xoshiro256StarStar
