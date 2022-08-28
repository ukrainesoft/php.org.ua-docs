Клас ComponereAbstractDefinition

-   [« Установка](componere.installation.html)
    
-   [Componere\\Abstract\\Definition::addInterface »](componere-abstract-definition.addinterface.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Клас ComponereAbstractDefinition
    

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

-   [Componere\\Abstract\\Definition::addInterface](componere-abstract-definition.addinterface.html) — Додає інтерфейс
-   [Componere\\Abstract\\Definition::addMethod](componere-abstract-definition.addmethod.html) — Додає метод
-   [Componere\\Abstract\\Definition::addTrait](componere-abstract-definition.addtrait.html) - Додає трейт
-   [Componere\\Abstract\\Definition::getReflector](componere-abstract-definition.getreflector.html) - Reflection