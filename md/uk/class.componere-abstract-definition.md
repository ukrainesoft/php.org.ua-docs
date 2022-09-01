---
navigation:
  - componere.installation.md: « Установка
  - componere-abstract-definition.addinterface.html: 'ComponereAbstractDefinition::addInterface »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас ComponereAbstractDefinition
---
# Клас ComponereAbstractDefinition

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

-   [ComponereAbstractDefinition::addInterface](componere-abstract-definition.addinterface.html) — Додає інтерфейс
-   [ComponereAbstractDefinition::addMethod](componere-abstract-definition.addmethod.html) — Додає метод
-   [ComponereAbstractDefinition::addTrait](componere-abstract-definition.addtrait.html) - Додає трейт
-   [ComponereAbstractDefinition::getReflector](componere-abstract-definition.getreflector.html) - Reflection
