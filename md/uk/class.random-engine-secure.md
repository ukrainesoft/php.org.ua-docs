---
navigation:
  - class.random-cryptosafeengine.md: « Random\\CryptoSafeEngine
  - random-engine-secure.generate.md: 'Random\\Engine\\Secure::generate »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\Engine\\Secure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\Engine\\Secure

(PHP 8 >= 8.2.0)

## Вступ

Створює криптографічно безпечну випадкову послідовність, використовуючи CSPRNG операційної системи.

Випадкова послідовність, що створюється [Random\\Engine](class.random-engine.md), підходить для всіх програм, включаючи створення довгострокових секретів, таких як ключі шифрування.

Механизм**Random\\Engine\\Secure** є рекомендованим безпечним вибором за умовчанням, якщо програма не вимагає відтворюваних послідовностей або дуже високої продуктивності.

## Огляд класів

```classsynopsis

    
     final
     class Random\Engine\Secure
    

    
     implements
      Random\CryptoSafeEngine {

    /* Методы */
    
   public generate(): string

   }
```

## Зміст

-   [Random\\Engine\\Secure::generate](random-engine-secure.generate.md)— Створює криптографічно безпечну випадкову послідовність
