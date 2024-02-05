---
navigation:
  - random-randomizer.unserialize.md: '« Random\\Randomizer::\_\_unserialize'
  - random-engine.generate.md: 'Random\\Engine::generate »'
  - index.md: PHP Manual
  - book.random.md: Random
title: Інтерфейс Random\\Engine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Random\\Engine

(PHP 8 >= 8.2.0)

## Вступ

Інтерфейс **Random\\Engine** забезпечує низькорівневе джерело випадкової послідовності, повертаючи випадкові байти, які споживаються високорівневими API для виконання своїх операцій. Інтерфейс **Random\\Engine** дозволяє міняти місцями алгоритм, який використовується для генерації випадкової послідовності, оскільки кожен алгоритм робить різні компроміси для відповідності конкретним умовам використання. Деякі алгоритми дуже швидкі, але створюють випадкову послідовність низької якості, тоді як інші алгоритми повільніші, але створюють якіснішу випадкову послідовність, аж до криптографічно безпечної випадкової послідовності, яку забезпечує механізм [Random\\Engine\\Secure](class.random-engine-secure.md)

PHP надає кілька двигунів **Random\\Engine** з коробки для різних випадків використання. Двигун [Random\\Engine\\Secure](class.random-engine-secure.md), заснований на CSPRNG, є рекомендованим безпечним вибором за умовчанням, якщо програма не вимагає відтворюваних послідовностей або дуже високої продуктивності.

## Огляд інтерфейсів

```classsynopsis

    
     interface Random\Engine {

    /* Методы */
    
   public generate(): string

   }
```

## Зміст

-   [Random\\Engine::generate](random-engine.generate.md) \- Створює випадкову послідовність
