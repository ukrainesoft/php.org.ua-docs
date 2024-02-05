---
navigation:
  - random-engine.generate.md: '« Random\\Engine::generate'
  - class.random-engine-secure.md: Random\\Engine\\Secure »
  - index.md: PHP Manual
  - book.random.md: Random
title: Інтерфейс Random\\CryptoSafeEngine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Random\\CryptoSafeEngine

(PHP 8 >= 8.2.0)

## Вступ

Інтерфейс, що вказує, що тип [Random\\Engine](class.random-engine.md) повертає криптографічно безпечну випадкову послідовність.

## Огляд інтерфейсів

```classsynopsis

    
     interface Random\CryptoSafeEngine

    extends
      Random\Engine {

    /* Наследуемые методы */
    
   public Random\Engine::generate(): string

   }
```
