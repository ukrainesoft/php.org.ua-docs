---
navigation:
  - componere.installation.md: « Встановлення
  - componere-abstract-definition.addinterface.md: 'Componere\\Abstract\\Definition::addInterface »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас Componere\\Abstract\\Definition
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Componere\\Abstract\\Definition

(Componere 2 >= 2.1.0)

## Вступ

Остаточний абстрактний клас є структурою класу і не повинен використовуватися програмістом.

## Огляд класів

```classsynopsis


    
    
     
      final
      abstract
      class Componere\Abstract\Definition
     
     {
    

    /* Методы */
    
   public addInterface(string $interface): Definition
public addMethod(string $name, Componere\Method $method): Definition
public addTrait(string $trait): Definition
public getReflector(): ReflectionClass

   }
```

## Зміст

-   [Componere\\Abstract\\Definition::addInterface](componere-abstract-definition.addinterface.md)— Додає інтерфейс
-   [Componere\\Abstract\\Definition::addMethod](componere-abstract-definition.addmethod.md)— Додає метод
-   [Componere\\Abstract\\Definition::addTrait](componere-abstract-definition.addtrait.md) \- Додає трейт
-   [Componere\\Abstract\\Definition::getReflector](componere-abstract-definition.getreflector.md)— Reflection
